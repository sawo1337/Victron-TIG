Go to your installation page on https://vrm.victronenergy.com/ then go to `Settings` > `General` - there is your VRM Portal ID

You need the below python script which you can run online here - https://www.onlinegdb.com/ByqR27fEL (click `fork this` and then change the portal id to yours):

With the output from that script, you can find which server your portal id connects to.

`vrm_portal_id = 'PORTAL_ID_HERE'

def _get_vrm_broker_url():
    sum = 0
    for character in vrm_portal_id.lower().strip():
        sum += ord(character)
    broker_index = sum % 128
    print (broker_index)
    
    
_get_vrm_broker_url()`

Then replace ["ssl://mqtt000.victronenergy.com:8883"] in telegraf.config with the value returned by the script. For example, if you get 125, then your url needs to be ["ssl://mqtt125.victronenergy.com:8883"]
