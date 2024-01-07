# mqtt-learnings


```
while true; do mosquitto_pub -t topic/state -m "Hello World $(date +'%s')"; sleep 2; done
```

# visualize

* Mac https://mqtt-explorer.com/
* Android https://play.google.com/store/apps/details?id=snr.lab.iotmqttpanel.prod

# setup
```
brew install mosquitto
```

```
mosquitto has been installed with a default configuration file.
You can make changes to the configuration by editing:
    /opt/homebrew/etc/mosquitto/mosquitto.conf

To restart mosquitto after an upgrade:
  brew services restart mosquitto
Or, if you don't want/need a background service you can just run:
  /opt/homebrew/opt/mosquitto/sbin/mosquitto -c /opt/homebrew/etc/mosquitto/mosquitto.conf
```


# config

```
listener 1883 0.0.0.0
listener 1883 192.168.178.71
allow_anonymous true
```


should trigger:
<img src="assets/firewall_mac.png"/>


# iotcloud

```
ArduinoIoTCloudTCP::handle_ConnectMqttBroker could not connect to mqtts-up.iot.arduino.cc:8884
ArduinoIoTCloudTCP::handle_ConnectMqttBroker 7 connection attempt at tick time 1642045
```

## issues
* AK9753 (https://www.sparkfun.com/products/14349) https://github.com/sparkfun/SparkFun_DataLogger/issues/17 
