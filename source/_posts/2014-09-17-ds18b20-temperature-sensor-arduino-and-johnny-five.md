title: DS18B20 Temperature Sensor, Arduino, and Johnny-Five
date: 2014-09-23 14:28:46
tags: [javascript, arduino, hardware, johnny-five, node.js]
---

I've been doing a bit of hardware hacking over the past week or so, and I'm really starting to get into it. I ordered some DS18B20 digital temperature sensors on Amazon, which I intend to use as part of a high-tech homebrew setup. When I received the sensors, I was pretty pumped to start using them, so I sat down and looked up instructions to connect them to an Arduino Uno.


It was pretty straightforward, though I had to improvise on the resistor, because I didn't have a 4.7K Ohm lying around (it turns out 5 1K resistors in series will suffice).


However, getting it to work with johnny-five was a bit harder. After lots of searching around, I came to the conclusion that the default firmware on the Arduino would not work out of the box with One-Wire sensors, and I'd have to install the ConfigurableFirmata library.

<!--more-->

There was not much documentation on how to do this, so for anyone Googling in the future, hopefully this will help! Here are the steps (directories are for OS X, so you'll have to find the proper directory on other platforms):

1. Get and install the arduino IDE from http://arduino.cc/en/Main/Software#toc1
2. Delete the built-in Firmata library:
```bash
rm -rf /Applications/Arduino.app/Contents/Resources/Java/libraries/Firmata
```
3. Clone the firmata library on the "configurable" branch into the Arduino libraries directory:
```bash
git clone git@github.com:firmata/arduino.git --branch configurable --single-branch /Applications/Arduino.app/Contents/Resources/Java/libraries/Firmata
```
4. Open the Arduino app and flash the board with the ConfigurableFirmata example:
  - Make sure you have your board selected under "Tools > Board" (in my case, "Arduino Uno")
  - "File > Examples > Firmata > ConfigurableFirmata"
  - Click "Upload"
5. That's it! You should now be able to use the One-Wire methods on the firmata object.

I was able to find an example of how to use it [in the johnny-five issue](https://github.com/rwaldron/johnny-five/issues/285#issuecomment-31485445). I've also posted a slightly more interesting example [here](https://github.com/lakenen/hardware-stuff/blob/master/ds18b20.js). In my example, the RGB LED changes color based on the temperature reading from the sensor.

Anyways, hopefully this article can save someone an hour or so of searching around!
