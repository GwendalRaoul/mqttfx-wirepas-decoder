# mqttfx-wirepas-decoder

This project contains an addon for the [MQTT.fx][mqttfx] application that can decode wirepas protobuf
message payloads.

The content of the messages are converted to Json format as depicted in this screenshot:

![Sreenshot][here_screenshot]

# Install

You can directly download a precompiled JAR from the [release tab][here_release].
The **mqttfx-wirepas-decoder_addon.jar** file should be placed in the MQTT.fx **addon** directory, which
varies by platform:

| OS          | Add-on location                                          |
|:------------|:---------------------------------------------------------|
| **macOS**   | `[USER_HOME]/Library/Application Support/MQTT-FX/addons` |
| **Windows** | `[USER_HOME]\AppData\Local\MQTT-FX\addons`               |
| **Linux**   | `[USER_HOME]/MQTT-FX/addons`                             |

# How to use

Once mqttfx is started and you have subscribed to some topics (like _gw-event/#_), you can select the Wirepas Generic Protobuf decoder in the "Payload decoded by" drop down menu in the right lower part of the screen.
It should decode the received message in a Json readable format.

> :warning:
>
> _Main purpose of this pluggin is to visualize the traffic to help diagnose the issues but is not designed nor tested with very high loaded brokers_
>


# Building

If you want to add your modification, you can rebuild it yourself.

The build uses Gradle. Build with the `shadowJar` task:

```
./gradlew shadowJar 
```

That will produce a `build/libs/mqttfx-wirepas-decoder-<version>-all.jar` which you can install as described bellow.

[mqttfx]: http://mqttfx.org/
[here_screenshot]: media/screenshot.png
[here_release]: https://github.com/GwendalRaoul/mqttfx-wirepas-decoder/releases

