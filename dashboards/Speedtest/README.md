## Known issues

please provide an issue

![](speedtest.png)
## Description

This dashboard gives an overview about the speedtest which is configured in iobroker. The preconditions please see below

## Installation / preconditions

1. Grafana version >9.3.x
2. InfluxDB version >2
3. InfluxDB is correctly installed and working in iobroker
4. Speedtest cli is installed on iobroker client --> [please find here official documentation](https://www.speedtest.net/apps/cli#ubuntu)
5. [javascript is correctly installed and configured from here](https://www.kreyenborg.koeln/speedtest-fuer-iobroker/)

Now:

6. Enable the follwoing datapoints in iobroker for influxdb logging:
a. the following ids / datapoints needed to be enabled in iobroker for InfluxDB2 logging:
+ javascript.0.Speedtest.Ergebnisse.Download_MB
+ javascript.0.Speedtest.Ergebnisse.Download_MBit
+ javascript.0.Speedtest.Ergebnisse.Ping
+ javascript.0.Speedtest.Ergebnisse.Upload_MB
+ javascript.0.Speedtest.Ergebnisse.Upload_MBit
+ javascript.0.Speedtest.Ergebnisse.Jitter
7. Influx database is configured in Grafana with FLUX !!!
8. Load the speedtest.json from here
9. Go into Grafana under DASHBOARDS / IMPORT and load via Upload JSON file
10. Click LOAD and your dashboard should appear !
11. Please select correct DATABASE and BUCKET --> values should appear !

## Changelog

* 0.0.2 - dashboard updated (06.01.2023)

+ changed to last instead of mean
+ difference deleted()
+ last measured time in dashboard added
+ new graph added for average speed per day
+ new curve added "jitter" in graph ping
+ picture updated

* 0.0.1 - first version (06.01.2023)