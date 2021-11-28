# flow.nodered.shelly3em

Statistics diagram for power use with Shelly 3 EM and InfluxDB on NR-Dashboard

Shows statistics from Shelly3EM on NR-Dashboard.

You need this nodes seperatly installed under "palette":

node-red-contrib-calc
node-red-contrib-influxdb
node-red-contrib-moment
node-red-contrib-ui-artless-gauge

What must be custmoized by you?

Influx Node with your db and take a look @function node: "fields and tags".
Mqtt Topic from Shelly
Path of Log file

What to do?
Prize calculation on changed prizes with correct historical data. eg: When change cost/month -> calculate prize from history until today with old cost/month but from now on with new cost/month and summarize it.

I will work on this.
If you have any suggestions, please let me know.
I'm thinking of doing this with an influx query.
