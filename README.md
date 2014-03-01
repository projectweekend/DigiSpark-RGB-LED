DigiSpark-RGB-LED
=================

A simple class for controlling a [DigiSpark](http://digistump.com/products/1) [RGB LED](http://digistump.com/products/3) via USB using Python.

The `arduino` package in this repo was borrowed from [DigiSpark Example Programs](https://github.com/digistump/DigisparkExamplePrograms/tree/master/Python/DigiBlink/source/arduino). This all came about when I was working on a headless Raspberry Pi based project ([Pi-Nova-5](https://github.com/projectweekend/Pi-Nova-5)) and wanted to use the DigiSpark LED as a status indicator. 

The two external Python dependencies are included in the `requirements.txt` file. The [webcolors](https://pypi.python.org/pypi/webcolors) package can be installed via `pip`. To install the [pyusb](https://github.com/walac/pyusb) package, follow instructions in that repo. After that, load the `DigiUSB→DigiBlink` example sketch onto your Digispark using the DigisparkArduino IDE.

Once everything is installed, simply plug the DigiSpark into a USB port on your computer and...

## Create an LED instance:
```
 from led import LED

 my_led = LED()
```

## Turn the LED on:
```
 # make it red
 my_led.on('red')

 # make it blue
 my_led.on('blue')

 # make it green
 my_led.on('green')
```

## Blink the LED:
```
 # blink red 3 times
 my_led.blink('red', 3)

 # blink blue 5 times
 my_led.blink('blue', 5)

 # blink green 10 times
 my_led.blink('green', 10)
```

## Turn the LED off:
```
 my_led.off()
```
