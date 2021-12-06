# flow.nodered.shelly3em

Statistics diagram for power use with Shelly 3 EM and InfluxDB on NR-Dashboard

Shows statistics from Shelly3EM on NR-Dashboard.

You need this nodes seperatly installed under "palette":
```
node-red-contrib-calc
node-red-contrib-influxdb
node-red-contrib-moment
node-red-contrib-ui-artless-gauge
```
What must be custmoized by you?
```
Influx Node with your db and take a look @function node: "fields and tags".
Mqtt Topic from Shelly
Path of Log file
```
Hint:

To store .flow. context variables in localfilesystem turn it on in settings.js:

https://nodered.org/docs/user-guide/context

In my example:
```
grep -C5 contextStorage .node-red/settings.js
    // Context Storage
    // The following property can be used to enable context storage. The configuration
    // provided here will enable file-based context that flushes to disk every 30 seconds.
    // Refer to the documentation for further options: https://nodered.org/docs/api/context/
    //
    contextStorage: {
        default: "file",
        memoryOnly: { module: 'memory' },
        file: { module : 'localfilesystem' }
        },
```
Otherwise you must backup and restore context variables on nodered restart.


What to do?
Prize calculation on changed prizes with correct historical data. eg: When change cost/month -> calculate prize from history until today with old cost/month but from now on with new cost/month and summarize it.

I will work on this.
If you have any suggestions, please let me know.
I'm thinking of doing this with an influx query.
