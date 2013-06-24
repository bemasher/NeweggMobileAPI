# NeweggMobileAPI
Information gleaned from sniffing traffic of the [Newegg Mobile](http://www.newegg.com/mobile) iOS app for iPhone.

## Sniffing Traffic
### Dumping Traffic
All traffic was analyzed by [Fiddler 2](http://fiddler2.com/) which compared with tcpdump appears to add or modify http headers in both requests and responses. Since the majority of the headers remain the same I am leaving any added headers in the requests and responses.

### Browsing the App
While sniffing traffic, all available options and browsable locations were visited inside the mobile application.

## Conventions
From this point forward a few conventions will be used for readability:
 * `###` will be used to denote that potentially personal data has been removed.
 * `...` indicates that there are multiples of the item the elipses follows, as in lists.

## Table of Contents
 * [Home](home.md)
 * [Searching](searching.md)