# dotnetcore-background-task

Example taken from [here](https://levelup.gitconnected.com/net-core-worker-service-as-windows-service-or-linux-daemons-a9579a540b77)


Added Systemd, and WindowsServices references

## On a Linux host:

- Run the console app as a background process, redirect the output to `/tmp/worker.log`
```bash
$ nohup dotnet run 2>&1 > /tmp/worker.log&
$ tail -f /tmp/worker.log
```

You'll see the timestamps increment showing you that the dotnet process is running in the background.

