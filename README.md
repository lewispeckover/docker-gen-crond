docker-gen-crond
=====
Converts discovered cronjobs into docker execs via [docker-gen](https://github.com/jwilder/docker-gen/).

The generated crond configuration can be used by the host or by a dedicated crond container.

Expose a single cron job via CRONJOB environment variable:
```
  docker run -it -e "CRONJOB=* * * * * /usr/bin/php /usr/local/cron.php >> /var/log/xyz.log" busybox /bin/sh
```

Multiple jobs can be exposed via additional variables CRONJOB_0 .. CRONJOB_9

