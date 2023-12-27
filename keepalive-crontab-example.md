#password can be hashed, haven't created an example for that yet

#make sure to replace mqtt000 with the id of the server you're connecting to

#make sure to update the location of venus-ca.crt if it's not in /etc/ssl/certs/venus-ca.crt

#without that keepalive message, you would only get messages in the first message

`* * * * * sleep 55;  mosquitto_pub -h mqtt000.victronenergy.com -p 8883 --cafile /etc/ssl/certs/venus-ca.crt -i zzr -u victron-portal-email@user.name -P 'victron-portal-password' -t 'R/<your-portal-id>/keepalive' -m ''`
