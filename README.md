# Victron-TIG
Victron monitoring with Telegraf, InfluxDB, and Grafana (optional android dashboard included) using Cerbo GX

The code here has been tested with InfluxDB 1.8.x OSS. It is recommended to use that as 1.8 is generally more user-friendly and stable. Quite possible that the Grafana queries would not work out of the box with InfluxDB 2.x+ I've kept away from raw queries, still worth the try if you really want to use newer Influx.

How to find the MQTT Server IP your installation needs to connect to is described in `find-mqtt-server-ip.md`

How to setup keepalive payload (on Unix) is described in `keepalive-crontab-example.md`

![image](https://github.com/sawo1337/Victron-TIG/assets/31248804/1f6f2dc4-f018-46a8-956c-676e1a089282)

![image](https://github.com/sawo1337/Victron-TIG/assets/31248804/9acbdec7-cb9e-40ef-a3a1-50f5089db12d)
