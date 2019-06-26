# Record the speed of your Wi-Fi connection

Think your Wi-Fi connection is slow and want a record to show your internet provider? Look no further :smiley:.

Each time the application is run, the wifi speed is recorded and appended to a results file.

```
{"ping":38,"download":21.2,"upload":18,"day":"24/06/2019","time":"16:50"}
{"ping":39,"download":22,"upload":17.6,"day":"24/06/2019","time":"17:50"}
{"ping":54,"download":22.8,"upload":18,"day":"24/06/2019","time":"18:50"}
```

## Install
```
npm install --global record-wifi-speed
```

## Usage
You can either run the application as an executable or with node.

Understandably you may not trust the executable. But the reason it's included is so that you can create a scheduled task which executes it periodically (for example with Windows Task Scheduler). It would then record your Wi-Fi speed in the background every period. You could package your own executable by cloning this project and running `npm run build`.

#### Arguments
- wifiName: The name of the Wi-Fi network you wish to record the speed of. For example `PLUSNET-1234`.
- recordLocation: The location of the file which will contain a record of the results. For example `C:\Users\Bob\wifi-speed-results.txt`.

### Option 1 - executable
```
bin/record-wifi-speed <wifiName> <recordLocation>
```

### Option 2 - node
```js
const recordWifiSpeed = require('record-wifi-speed')

recordWifiSpeed({
  wifiName: '...',
  recordLocation: '...',
})
```
