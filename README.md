# mqttfx-wirepas-decoder

This project contains an addon for the [MQTT.fx][mqttfx] application that can decode wirepas protobuf
message payloads.

The content of the messages are converted to Json format as depicted in this screenshot:

![Sreenshot][here_screenshot]

# Install

You can directly download a precompiled JAR from the [release tab][here_rlease].
The **mqttfx-wirepas-decoder-(version)-all.jar** file should be placed in the MQTT.fx **addon** directory, which
varies by platform:

| OS          | Add-on location                                          |
|:------------|:---------------------------------------------------------|
| **macOS**   | `[USER_HOME]/Library/Application Support/MQTT-FX/addons` |
| **Windows** | `[USER_HOME]\AppData\Local\MQTT-FX\addons`               |
| **Linux**   | `[USER_HOME]/MQTT-FX/addons`                             |


# Building

The build uses Gradle. Build with the `shadowJar` task:

```
./gradlew shadowJar
```

That will produce a `build/libs/mqttfx-wirepas-decoder-<version>-all.jar` which you can install as described bellow.

[mqttfx]: http://mqttfx.org/
[here_screenshot]: media/screenshot.png
[here_release]: releases
