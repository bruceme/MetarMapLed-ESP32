# ESP_METAR - ESP-32 Based Aviation Weather Map

## Core harware

* **ESP-32** - This branch is intended to be a minimum MetarMap implimentation running on any
  ESP-32 platform.  Typical implimentation is using a feather clone.

* **Make it yours**
  * Update your network SSID & Password in the wifi_config.h file
  * Update the list of airports you wish to monitor

* **Firmware build**
  * Clone this repository
  * Build using Platformio, it should pull all required dependencies
  * Download to your ESP-32 device using platformio tools

* **WS2812B-F5 LEDs** - One per airport/weather station.  
  These are RGB "neo pixels" in a standard 5mm LED form factor.  They have 
  four pins: data-in, data-out, GND, and Vcc.  There appear to be two 
  different pinouts available.  This project uses the "WorldSemi" version:

    * P1: DOUT (short pin, next to flat edge)
    * P2: VCC (longest pin)
    * P3: GND (medium length pin)
    * P4: DIN (short pin)

  The other version's pinout has two long pins and two short pins.  If you 
  have access to these, they can be used, but not with the LED PCBs

  I purchased LEDs from this [eBay listing](https://www.ebay.com/itm/234203893644)
  and from [Aliexpress](https://www.aliexpress.us/item/2255800693144395.html)

## Arts and Crafts
* **Airport poster** - The original source material for my poster was from the 
  official FAA 
  [VFR Raster Charts](https://www.faa.gov/air_traffic/flight_info/aeronav/digital_products/vfr/)
  page.  This site has high-resolution PDFs available of all
  of the US raster charts.  Other countries will likely have the same resources
  available, but I don't have links to those, yet.

  I had my map printed on 1/4" foam-core posterboard at a local print shop.
  The printing was about $20.00.  They will also trim the poster down to 
  size, or you can print registration marks and cut it yourself.

* **Picture Frame** - I used a 16x20 shadow box frame from Michael's craft 
  store.  Having the depth is nice, because it allows the frame to sit flush
  against the wall when hung.

* **Power supply** - 2A or larger USB power supply is required.
  The CPU board has a USB-C connector for power input.  You can also run it
  on a power-bank-type battery tucked into the frame, but LEDs are pretty 
  power hungry, and the software doesn't currently use any of the low-power
  features of the ESP-32.  My prototype, with about 42 airports/LEDs uses about
  500ma-600ma when running at full brightness.

* **Wire** - One of the most tedious parts of building the map is wiring the 
  LEDs (keep that in mind when you decide to put every podunk airport within
  100 miles on your map!).  You need four-conductor wire for the LEDs, I 
  used [this spool](https://www.amazon.com/dp/B08J7WKV6W) of wire from Amazon.
  In hindsight, I wish that I had used 24 gauge wire instead of 22, because
  this wire was pretty stiff in short lengths for close-together airports.

* **LED Clips** - These add a nice finished look to the LEDs, holding them 
  securely in the foam core board.  I used these 
  [BIVAR C-105-SR](https://www.mouser.com/ProductDetail/749-C-105-SR) that 
  I purchased from Mouser.  

  You could also use hot glue, but it won't be as "pretty".

# Recomennded Tools

These tools are absolutely required:

* **Soldering Iron** - Fine tip.  You have one of these, right?
* **Wire Cutters** - Any kind will do.  
* **X-Acto Knife** - The "Kleenex of Cutters" -- any sharp hobby knife 
  will do.  If you need to cut the foam core, make sure that you have a 
  bunch of extra blades, because foam core dulls blades quickly!

These tools aren't strictly necessary, but made assembly MUCH easier:

* **Foam-Core Hole Drill** - Makes nice clean holes in foam-core board.  You
  could use an exacto knife, but these are a huge time saver.   I got mine
  from Amazon: 
  [Logan WD8011 FoamWerks Foamboard Hole Drill](https://www.amazon.com/dp/B007L6EUJ8)
* **Wire strippers** - This project uses a LOT of wire connections, and your 
  mother told you not to use your teeth for stripping wire!  I use these:
  [Klein Tools 11061 Wire Stripper / Cutter](https://www.amazon.com/Self-Adjusting-Stripper-Klein-Tools-11061/dp/B00CXKOEQ6/).
* **Flush Cutters** - For trimming the LED leads after soldering.  I use 
  these: [Weller 170MN Xcelite General Purpose Shearcutter](https://www.amazon.com/dp/B00B886R2I).
