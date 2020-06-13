# esprit-board

<img src="Esprit_Rendered.png" align="right" height="210px" hspace="5px"/>

This repository contains the [schematics][1], BOM ([CSV][2], [PDF][3]), [Gerber files][4], and [Proteus project][5] for a ESP32-based board capaple of running ClojureScript. These boards are designed to be used with the [Esprit REPL][6].

> Note: You don't need to use this particilar board to run ClojureScript. Any ESP32 WROVER with 8 MiB SPIRAM is capable of running a ClojureScript REPL. 

## Make One

The files in this repository are open source. Feel free to use them to understand how things work, use the Gerbers and BOM to make your own boards, etc.

## Buy One

<a href="https://www.tindie.com/stores/fikesfarm/?ref=offsite_badges&utm_source=sellers_mfikes&utm_medium=badges&utm_campaign=badge_medium"><img align="right" src="https://d2ss6ovg47m0r5.cloudfront.net/badges/tindie-mediums.png" alt="I sell on Tindie" width="150" height="78"></a> If you'd like to buy one pre-assembled and tested they are [available on Tindie][7].

> Note: If Tindie indicates they are sold out, we're making more (generally a new batch should be available within a week.)

_The intent is to not profit but instead sustainably make small batches of hand-asembled boards available to the community for fun and experimentation._

## USB

The board uses a Silicon Labs CP2102N USB to UART chip. If needed, the drivers for various OSs are available [here][8].

The board comes with a micro-USB connector.

## Power / Batteries

The board has circuitry that allows it to run either from power obtained from the micro-USB connetion or from power supplied by a lithium ion polymer ("lipo
") battery. You can dynamically switch between the two and the ESP32 will continue to run uninterrupted so long as either is connected.

If you have both USB and a battery connected, the board has an onboard IC (an MCP73833T) that is used to properly charge the lipo battery. In short, it behaves much like a modern cellphone.

As a safety mechanism, an onboard thermistor is included which will [suspend battery charging](https://youtu.be/U56QTjNAHnw) if the board is detected as being too warm.

Here are batteries that have been successfully used with the board:

- [Adafruit 100 mAh][9]
- [Adafruit 1200 mAh][10]
- [Adafruit 2400 mAh][11]

[1]:	esprit-board.PDF
[2]:	Bill%20Of%20Materials%20Esprit.csv
[3]:	Bill%20Of%20Materials%20Esprit.pdf
[4]:	esprit-board%20-%20CADCAM.ZIP
[5]:	esprit-board.pdsprj
[6]:	https://github.com/mfikes/esprit
[7]:	https://www.tindie.com/products/fikesfarm/esprit-clojurescript-repl/
[8]:	https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers
[9]:	https://www.adafruit.com/product/1570
[10]:	https://www.adafruit.com/product/258
[11]:	https://www.adafruit.com/product/328
