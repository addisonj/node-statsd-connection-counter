#
A quick and dirty module to count connections for servers and agents

## Why?
If you are using the http Agent, and you throw to many connections to the same host, you are going to get slow.

This tells you how many sockets you have open, as well as the length of your request queue.

It also takes an http server and counts the number of incoming connections

## How?

``` JavaScript
var SDC = require("statsd-client")

var sdc = new SDC()
var myServer = http.createServer() //or an express server object
var connCounter = require("statsd-connection-count")

connCounter(sdc, myServer, 1000)
```
