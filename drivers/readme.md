These are the software driver implementations I have identified so far.

## Adafruit (Python)

https://github.com/adafruit/Adafruit_MAX31856

## Dj Kilgore (ESP32)

https://github.com/djkilgore/max31856

There is some interesting comment in this implementation :

```
The private functions which read and write the registers of the chip are a bit of a hack, they send each byte in a seperate transaction and manually control the SPI CS line.

From what I can tell the MAX31856 expects dummy bytes or "dead air" in between each byte sent and I wasn't able to replicate this with the ESP-IDF spi-master driver but I am probably doing something wrong.
```

```
After I finished the library, I had to go back and add a read_fast_register() function because the Fault register works like it should in a single transaction and was returning bad data with the hack.

I am going to assume this is some weird hardware issue with this chip until further notice or someone else submits a patch.
```


## Peter Easton (Arduino)

https://github.com/engineertype/MAX31856

## Stephen Smith (Python)

https://github.com/steve71/MAX31856
