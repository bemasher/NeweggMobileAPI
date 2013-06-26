# NeweggMobileAPI
Information gleaned from sniffing traffic of the [Newegg Mobile](http://www.newegg.com/mobile) iOS app for iPhone.

## Sniffing Traffic
### Dumping Traffic
All traffic was sniffed and analyzed using [Fiddler 2](http://fiddler2.com/).

### Browsing the App
While sniffing traffic, all available options and browsable locations were visited inside the mobile application.

## Conventions
From this point forward a few conventions are used to improve readability:
 * `...` indicates that there are multiples of the item the elipses follows or leads, as in lists.
 * Unless stated otherwise, all requests are absolute and directed at: http://www.ows.newegg.com/

## Table of Contents
 * [Home](home.md)
 * [Browsing](browsing.md)
 * [Searching](searching.md)
 * [Filtering](filtering.md)
 * [Items](items.md)

## TODO
 * Add golang type structures for encoding requests and decoding responses.
 * Generate tree of all current Newegg Stores > Categories > Sub-Categories.