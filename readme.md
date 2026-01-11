# MAX31856 Precision Thermocouple to Digital Converter with Linearization

# Background

This is a **temporary** repository destined to gather all sorts of information about and around the MAX31856. I will try and accumulate a maximum of sources around the chip and its application. 

The circuit is infamously known to pose a lot of issues. I came across these when looking for a high-temperature kiln controller and it quickly became clear that the proposed solutions might not be reliable enough for my application : too many users facing all sorts of problems that seem to originate from the MAX31856.

## Hypothesis

Starting with the basic assumption that the chip itself is reliable, the root of the problems could be either
1. the hardware implementation. By this I understand the schematic of the interface board, often an Adafruit Universal Thermocouple Amplifier MAX31856 Breakout or one of the many clones. An Adafruit board currently goes for $17, the MAX31856 evaluation board at Digikey is at $140. There may me a difference beyond volume and marketing.
2. the hardware implementation II. People have noticed wild variations of the mounted components, capacitors mostly, vs. the recommended values in the spec sheet.
3. the chip. There may be series of defective or counterfeit MAX31856 chips that have been put into circulation.
4. the driver implementation that handles the communication between the chip and the application
5. the application software - software bugs are not unheard of
6. the cabling - especially during evaluation or at hobby level, people may think that breadbords and Dupond cables are perfect. They are not.

This list likely isn't exhaustive.

## Official sources

https://www.analog.com/en/products/max31856.html

Evaluation board : https://www.analog.com/en/resources/evaluation-hardware-and-software/evaluation-boards-kits/max31856evsys.html

FAQ  : https://ez.analog.com/search?engineerzone%5Bquery%5D=MAX31856

Maxim (the original maker of the chip) has made a nice introductionary video that hasn't made it's way on the Analog website : https://www.digikey.com/en/videos/m/maxim-integrated/how-to-measure-temperature-using-rtds-and-the-max31865evkit


## Boards

adafruit

https://www.electronics-lab.com/project/precision-thermocouple-amplifier-thermocouple-to-digital-converter-with-linearization-spi-interface/

