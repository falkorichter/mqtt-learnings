# mqtt-learnings


```
while true; do mosquitto_pub -t topic/state -m "Hello World $(date +'%s')"; sleep 2; done
```

# visualize

* Mac https://mqtt-explorer.com/
* Android https://play.google.com/store/apps/details?id=snr.lab.iotmqttpanel.prod

# config

```
listener 1883 0.0.0.0
listener 1883 192.168.178.71
allow_anonymous true
```
