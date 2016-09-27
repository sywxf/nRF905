#nRF905 AVR/Arduino Library/Driver

<a href="http://www.nordicsemi.com/eng/Products/Sub-1-GHz-RF/nRF905">Nordic nRF905</a> Radio IC library for Arduino and AVR microcontrollers.


##Documentation
<a href="http://zkemble.github.io/nRF905/">Doxygen pages</a>


##Installing
###Arduino
Copy the arduino/nRF905/ folder to your Arduino libraries folder.

If you are using Arduino 1.5 then you will need to move the .cpp and .h files into the src folder.

Add

    #include <nRF905.h>
	#include <SPI.h>

to the top of the sketches that use the library.

Also have a look at nRF905_config.h, that's where you can change which pins are used and stuff.

###AVR
Copy the nRF905 folder to your project and add

    #include "nRF905/nRF905.h"

to the source files that use the library.

Examples in the examples folder.

--------

http://blog.zakkemble.co.uk/nrf905-avrarduino-librarydriver/

--------

Zak Kemble

contact@zakkemble.co.uk

###use
typedef enum
{
// NOTE:
// When using NRF905_BAND_868 and NRF905_BAND_915 for calculating channel (NRF905_CALC_CHANNEL(f, b)) they should be value 0x01,
// but when using them for setting registers their value should be 0x02.
// They're defined as 0x02 here so when used for calculating channel they're right shifted by 1

	NRF905_BAND_433 = 0x00,	/**< 433MHz band */
	NRF905_BAND_868 = 0x02,	/**< 868MHz band */
	NRF905_BAND_915 = 0x02	/**< 915MHz band */
} nRF905_band_t;
nRf905_setFrequency(433200000UL,nRF905_band_t);


