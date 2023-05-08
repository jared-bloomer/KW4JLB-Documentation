Setting up a Link Radio with a Morotola MaxTrac VHF Radio and a RIM-Maxtrac URI
===============================================================================

In some cases, you can not setup an allstarlinux node at a repeater site and attach it directly to your repeater. So what do you do? Well you have 2 options. First option is do nothing and no linking capabilities. the Second option is an RF link radio from a remote location. Here we will discuss the latter of the options. 

In preperation for this project there are several items we will need to gather. Below is a parts list of each of those items. 

+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Item                                               | QTY | Where to Buy                                                                                                                                                                                                                                                                             |
+====================================================+=====+==========================================================================================================================================================================================================================================================================================+
| Motorola Maxtracs VHF Radio                        |  1  | `Ebay.com <https://www.ebay.com/sch/i.html?_nkw=motorola+maxtrac+vhf&_sop=12>`_                                                                                                                                                                                                          |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Mini UHF to UHF Adapter                            |  1  | `Amazon.com Mini UHF to UHF Adapter <https://www.amazon.com/Female-SO239-PL259-Connector-Adapter/dp/B011KJ7RAK/ref=asc_df_B011KJ7RAK?tag=bngsmtphsnus-20&linkCode=df0&hvadid=80195746822994&hvnetw=s&hvqmt=e&hvbmt=be&hvdev=c&hvlocint=&hvlocphy=&hvtargid=pla-4583795273720137&psc=1>`_ |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Motorola MaxTracs Programming Software and Cables  |  1  | **Good Luck. A Club member had them on hand for us.**                                                                                                                                                                                                                                    |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| RIM-MaxTracx URI                                   |  1  | `Repeater-Builder <https://www.repeater-builder.com/products/usb-rim-lite.html>`_                                                                                                                                                                                                        |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Raspberry Pi 3B                                    |  1  | `Adafruit Raspberry Pi 3B <https://www.adafruit.com/product/3055>`_                                                                                                                                                                                                                      |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Micro Sd Card (16GB or larger)                     |  1  | `Amazon.com SanDisk Ultra 64GB Micro SD Card <https://www.amazon.com/SanDisk-Ultra-microSDXC-Memory-Adapter/dp/B0B7NXBM6P/ref=sr_1_4?crid=3K4TD2ZF0QQ8B&keywords=Micro%2BSD%2Bcard&qid=1683210442&sprefix=micro%2Bsd%2Bcard%2Caps%2C93&sr=8-4&th=1>`_                                    |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Raspberry Pi Case                                  |  1  | `Amazon.com Raspberry Pi Case <https://www.amazon.com/dp/B07PNB7JWP?psc=1&ref=ppx_yo2ov_dt_b_product_details>`_                                                                                                                                                                          |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Raspberry Pi Heatsinks                             |  1  | `Amazon.com Raspberry Pi Heatsinks <https://www.amazon.com/Angel-Mall-Raspberry-Heatsink-Transfer/dp/B07CZ1T27V/ref=sr_1_10?keywords=raspberry%2Bpi%2Bheatsink%2Bkit&qid=1683209861&sprefix=raspberry%2Bpi%2Bheast%2Caps%2C93&sr=8-10&th=1>`_                                            |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Raspberry Pi Power Supply                          |  1  | `Amazon.com Raspberry Pi Power Supply <https://www.amazon.com/Listed-iUniker-Raspberry-Supply-Switch/dp/B0B79FVPQ4/ref=sr_1_3?crid=16BD0E1AGZZOC&keywords=raspberry+pi+3+power+supply&qid=1683210340&sprefix=raspberry+pi+3+power+supply%2Caps%2C91&sr=8-3>`_                            |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Industrial 12V 30A Switching Power Supply          |  1  | `Amazon.com 12V 30A Power Supply <https://www.amazon.com/dp/B08LDC41B6?ref=ppx_yo2ov_dt_b_product_details&th=1>`_                                                                                                                                                                        |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Wires for Power Supply                             |  ~  | Local Big Box Store (Lowes, Home Depot, etc.)                                                                                                                                                                                                                                            |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PL-259 (UHF) Connectors                            |  4  | `Amazon.com PL-259 Connectors <https://www.amazon.com/Amphenol-PL259-Connectors-Solder-83-1SP-15RFX/dp/B083PPHMM5>`_                                                                                                                                                                     |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Davis RF Bury Flex (LMR400)                        |  ~  | `Ham Radio Outlet Davis RF Bury Flex <https://www.hamradio.com/detail.cfm?pid=H0-011882>`_                                                                                                                                                                                               |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| MFJ-1852 VHF Yagi Antenna                          |  1  | `Ham Radio Outlet MFJ-1852 Antenna <https://www.hamradio.com/detail.cfm?pid=H0-016756>`_                                                                                                                                                                                                 |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Polyphaser IS-50UX-C0 Lightening Arrestor          |  1  | `DX Engineering Polyphaser IS-50UX-C0 Lightening Arrestor <https://www.dxengineering.com/parts/ppr-is-50ux-c0>`_                                                                                                                                                                         |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PL-259 to SO-239 90 Degree Adapter                 |  1  | `Amazon.com PL-259 to SO-236 90 Degree Adapter <https://www.amazon.com/dp/B07P7Z9DG7?psc=1&ref=ppx_yo2ov_dt_b_product_details>`_                                                                                                                                                         |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Coax Seal                                          |  1  | `Amazon.com Coax-Seal <https://www.amazon.com/Fittings-Universal-Waterproof-Non-Conducting-Wire/dp/B00UZWM1U0/ref=sr_1_3?keywords=coax+seal&qid=1683555591&sr=8-3>`_                                                                                                                     |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 3M Super 33+ Tape                                  |  1  | `Amazon.com 3M Super 33+ Electrical Tape <https://www.amazon.com/MMM06132-Scotch-Super-Vinyl-Electrical/dp/B001DPPHS6/ref=sr_1_10?crid=3GYIP0OC5VWC5&keywords=3m+super+33%2B&qid=1683555643&sprefix=3m+super+33%2B%2Caps%2C95&sr=8-10>`_                                                 |
+----------------------------------------------------+-----+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Some additional items you may want depending on your install would be things like SO-239 Bulkhead connectors, Nylon/Plycarbonate Wall Plate Blank Covers, etc. The PL-259 to SO-239 90 Degree Adapter in the list above is just so the coax coming up from the floor to the wall does not have to be bent to get to the radio jumper. 

Antenna Installation
--------------------

First, thing is to determine the line of sight path from your antenna installation location and the repeater. I like to use `Ubiquiti's WISP (https://ispdesign.ui.com/#) <https://ispdesign.ui.com/#>`_ tool for this. 

For this particular installation I determined I only needed the MFJ-1852 Yagi antenna 6 feet off the ground. Due to the nature of where I was installing it, I installed it at 10 feet. Unfortunately for me the mounting hardware that comes with the Antenna if for a 1" pipe and I was mounting on a 1.5" pipe. With that said I had to get creative and build my own mounting bracket from 2" aluminum flat bar, some Long M6 Stainless Bolts, washers, nuts, and a 1.5" U-bolt. All this was found at Lowes. 

Once I mounted the Antenna, MFJ suggest attaching the short coax run for the driven element to the boom using electrical tape. I did so in 2 places so the SO-239 connector was hanging right near the Antenna Mast. This will help secure the coax later and allow for some strain relief. 

Next up was Cutting a peice of Davis RF Bury Flex (LMR400) Coax and Soldering on some PL-259 connectors. I ended up cutting around 15 feet of Coax for this particular installation. I like my connectors to look as professional as possible so I slip on a 3" peice of 1/2" Heatshrink with the glue on the inside, then my PL-259 barrel connector. I attached the inner connector of the PL-259, screwed on the barrel connector, then covered the end witht he heat shrink and sealed it all up but heating the heat shrink.

I then took the Davis RF Coax and attached it to the Antenna. I sealed the connections but taking 3M Supper 33 Tape and starting just below the PL-259 connector and wraping with overlaps to just above the SO-239 on the Antenna. I then started just below the Super 33 Tape with Coax Seal and again with overlapping wrap went just above the Super 33 Tape. I then massaged the coax seal to get it to properly stick as needed and seal it up. After than I pulled out the super 33 tape gain and started just below the coax seal and overlapping, I wraped all the way up above the coax seal, and then back down below the coax seal. 

.. image:: /_static/images/howtos/allstarlinux/rim-maxtrac/sealedcoax.jpeg

After doing all that, all that is left is securing the Davis RF Bury Flex Coax to the Mast and tidying things up. For this I just used Zip Ties (Yes I know they break down when exposed to UV so every few years I replace them as part of my on-going maintenance. Don't be a sad ham.)

Final Antenna Installation (Yes I know I need to clean my house, gutters, etc.)

.. image:: /_static/images/howtos/allstarlinux/rim-maxtrac/MFJ-1852.jpeg

Power
-----

For safety reason I will not go into how to wire up an industrial switching power supply. Here is a picture of the 12 volt 30 amp switching power supply I am using for this project.

.. image:: /_static/images/howtos/allstarlinux/rim-maxtrac/switching_psu.jpg

A Polyphaser IS-50UX-C0 Lightening Arrestor was installed to protect the Coax before it entered the structure. This is to help prevent any damage from a lightening strike. 

.. image:: /_static/images/howtos/allstarlinux/rim-maxtrac/lightening_arrestor1.jpg

.. image:: /_static/images/howtos/allstarlinux/rim-maxtrac/lightening_arrestor2.jpg

.. image:: /_static/images/howtos/allstarlinux/rim-maxtrac/lightening_arrestor3.jpg

Radio and RIM-MaxTrac URI
-------------------------

As far as the Radio goes, we have a Motorola Maxtrac VHF 45W Radio. Since this is an older radio, an old computer running DOS with a serial port is needed to program this radio. Due to that getting screen shots of the programming software is just ugly since I would be taking a picture of a computer screen and that never comes out well. You need to connect the RIB to the serial Port on the computer and then use the programming cable from the RIB to the MIC input on the radio. Also depending on the firmware on the radio the version of the Maxtrac software that works will vary. For us this was a lot of trial and error to find the right version. The key thing to programming the radio though is under additional programming where you can setup the various pins on the back on the radio. Pin 8 and 12 need to be set to HIGH and the set for specific purposes. This can be found as a note on the bottom of the `RIM-Maxtrac Schematic <https://www.repeater-builder.com/products/RIM_pdfs/RB_RIM_Max.pdf>`_ .

Here you can see the RIM-MaxTrac attached to the 16 pin connector on the back of the Motorola Maxtrac radio. 

.. image:: /_static/images/howtos/allstarlinux/rim-maxtrac/RIM-MaxTrac.jpg

The RIM-MaxTrac is connected to a Raspberry Pi 3B via a USB Cables

.. image:: /_static/images/howtos/allstarlinux/rim-maxtrac/rpi.jpg

The rest of the magic happens on the Raspberry Pi with the configuration of `Hamvoip <https://hamvoip.org/>`_ .