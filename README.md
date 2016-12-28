ansible influxdb cluster playbook
=================================

####configuration overview

The goal of this playbook is to make use of [InfluxDB](https://influxdb.com) as a system metric store.
Features:

* Can automatically cluster n-number of influxdb nodes
* Uses [Telegraf](https://github.com/influxdb/telegraf) to gather metrics using UDP
* Sets up [Kapacitor](https://github.com/influxdb/kapacitor) for processing, monitoring, and alerting
* Sets up a grafana dashboard
* Sets up downsampling for all metrics

####notes

* All of the packages in this repo are set to state=latest so that I don't have
to continuously maintain the version pin.
If you intend to use this in production you should pin all of the versions and
do testing between upgrades.
Additionally the influxdb modules make a lot of assumptions about the way influx
does things and are vulnerable to being broken between versions.

####requirements

CentOS 7

####install process

* Update inventory/hosts file with actual IP's
* Run site.yml playbook      

####influxdb admin site

    http://private_ip:8083

####grafana dashboard

    http://private_ip:3006


