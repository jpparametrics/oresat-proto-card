# "oresat-proto-card"

This is the "prototype" card for OreSat, meant to pioneer future cards and test the backplane, and be an 
easy way to hack in functionality. NOT MEANT FOR FLIGHT.

## Features

- Populates the two 1.27 mm connectors from the backplane.
- Populates all three SMPM RF connectors from the backplane.
- Standard TPS63070-bsaed buck/boost SPS (Vin = 2.5 to 7 V)
- Has our standard/favorite STM32F042K6 microcontroller.
   - With SWD, UART (FTDI), and CAN (to the backplane).
- Has lots of breakouts, but DO NOT POPULATE THE 0.1 IN CONNECTORS, THEY'RE TOO TALL!!!

![OreSat ProtoCard Picture](https://github.com/oresat/oresat-proto-card/blob/master/oresat-proto-card.png)

## Connector information

- Main 1.27 mm connector ("Center" connector)
   - Samtec TFM-120-01-L-D-RA
   - https://www.digikey.com/products/en?lang=en&site=US&keywords=TFM-120-01-L-D-RA
   - Drawing: http://suddendocs.samtec.com/prints/tfm-1xx-xx-xxx-d-xxx-mkt.pdf
   - Brochure: http://suddendocs.samtec.com/catalog_english/tfm.pdf
   - 3D CAD: https://www.samtec.com/partnumber/tfm-120-01-l-d-ra?vendor=digikey#technical
   - Notes: the -RE1 model is better because of the solder stakes, but the female connector doesn't fit! The stakes get in the way :(

- Auxiliary 1.27 mm ("alt-left" connector)
   - Samtec TFM-110-01-L-D-RA

- RF (70 cm, L band, S band) conenctors
   - Card
      - Molex 73300-0030 (possible replacement is 73300-0020 but it has full detent that we don't want)
      - SMPM Connector Plug, Male Pin 50 Ohm Board Edge, Cutout; Surface Mount Solder, smooth bore
      - Molex w/3D: https://www.molex.com/molex/products/datasheet.jsp?part=active/0733000030_RF_COAX_CONNECTORS.xml
   - Barrell (connects card to backplane)
      - Molex 73300-0220 (alt but slightly different lengths: -0223, -0228)
      - SMPM female to female barrel adapter 
      - RF Adapters - In Series SMPM JACK/JACK BULLET .21IN
      - Molex w/3D: https://www.molex.com/molex/products/datasheet.jsp?part=active/0733000220_RF_COAX_CONNECTORS.xml

