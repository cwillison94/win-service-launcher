# win-service-launcher
runs as a service and launches non-service applications

## dev environment
[Microsoft.NET v3.5](https://dotnet.microsoft.com/download/thank-you/net35-sp1)
[7zip](https://www.7-zip.org/download.html)
[SharpDevelop](http://www.icsharpcode.net/OpenSource/SD/Download/Default.aspx#SharpDevelop5x)

## how to install


## setting up 'launchers'
### types of launcher schedules
#### OnInterval
Launches process at given intervals
Parameters: name, filepath, filename, arguments, interval (ms)

#### OnTimeOfDay
Launches application process at given intervals
Parameters: name, filepath, filename, arguments, time

#### OnStartup
Launches application process when the service is being started
Parameters: name, filepath, filename, arguments, time

#### OnShutdown
Launches application process when the service is being shutdown
Parameters: name, filepath, filename, arguments

#### KeepAlive
Launches application process when the service is being started, then continuously monitors the process to make sure it is always running.
Parameters: name, filepath, filename, arguments, processName

### Example XML configuration file
```xml
<?xml version="1.0" encoding="utf-8"?>
<WinServiceLauncher version="0.0.0.42">
	<Launcher name="Sample Node.JS Service" working-path="c:\my-node-app\" command="npm" arguments="start">
		<OnStartup/>
	</Launcher>
</WinServiceLauncher>
```

