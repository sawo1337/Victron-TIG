#password can be hashed, haven't created an example for that yet

#make sure to replace mqtt000 with the id of the server you're connecting to

#make sure to update the location of venus-ca.crt if it's not in /etc/ssl/certs/venus-ca.crt

#make sure to install mosquitto on your distro before running the crontab!

#without that keepalive message, you would only get messages in the first message

#warning! If you are using Windows, you need to install Mosquitto for Windows and then set up a scheduled task to execute the same command as below every 55 seconds (make sure to copy only from mosquitto_pub onwards since the part before that is crontab-specific).

`* * * * * sleep 55;  mosquitto_pub -h mqtt000.victronenergy.com -p 8883 --cafile /etc/ssl/certs/venus-ca.crt -i zzr -u victron-portal-email@user.name -P 'victron-portal-password' -t 'R/<your-portal-id>/keepalive' -m ''`
