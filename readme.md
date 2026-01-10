# MAX31856 Precision Thermocouple to Digital Converter with Linearization

# Background

This is a **temporary** repository destined to gather all sorts of information about and around the MAX31856. I will try and accumulate a maximum of sources around the chip and its application. 

The circuit is infamously known to pose a lot of issues. I came across these when looking for a high-temperature kiln controller and it quickly became clear that the proposed solutions are not reliable enough for my application : far too many users facing all sorts of problems that seem to originate from the MAX31856.

## Hypothesis

Starting with the basic assumption that the chip itself is reliable, the root of the problems could be either
1. the hardware implementation. By this I understand the schematic of the interface board, often an Adafruit Universal Thermocouple Amplifier MAX31856 Breakout or one of the many clones. An Adafruit board currently goes at $17, the MAX31856 evaluation board at Digikey is at $140. There may me a difference beyond volume and marketing.
2. the chip. There may be series of defective MAX31856 chips that have been put into circulation.
3. the driver implementation that handles the communication between the chip and the application
4. the software implementation - software bugs are not unheard of
5. the cabling - especially during evaluation or at hobby level, people may think that breadbords and Dupond cables are perfect. They are not.

This list likely isn't exhaustive. Please help fill in the gaps.

## Official sources

[[MAX31856.pdf]]

https://www.analog.com/en/products/max31856.html

FAQ  : https://ez.analog.com/search?engineerzone%5Bquery%5D=MAX31856

Maxim (the maker of the chip) (now Analog Devices) has made a nice introductionary video that hasn't made it's way on the Analog website : https://www.digikey.com/en/videos/m/maxim-integrated/how-to-measure-temperature-using-rtds-and-the-max31865evkit


