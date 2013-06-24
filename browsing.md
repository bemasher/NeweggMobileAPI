# Browsing
## Top-Level Menu
The top-level menu which is first presented when clicking Browse contains a list of stores available. To browse sub-categories of each store only the `StoreID` field is required.

### Request
```
GET /Stores.egg/Menus HTTP/1.1
Host: www.ows.newegg.com
Accept-Language: en-us
Pragma: no-cache
User-Agent: Newegg iPhone App / 3.1.2
X-HighResolution: true
Accept: */*
Connection: keep-alive
MobileVisitor: VERSIONINFO=iPhone App 3.1.2
X-Signature: ###
Cookie: ###
Connection: keep-alive
X-Timestamp: 1372063240.046852
Accept-Encoding: gzip, deflate
```

### Response
```
HTTP/1.1 200 OK
Cache-Control: private
Content-Type: application/json; charset=utf-8
Content-Encoding: gzip
Vary: Accept-Encoding
Server: Microsoft-IIS/7.5
X-AspNetMvc-Version: 1.0
X-AspNet-Version: 2.0.50727
Set-Cookie: ###
Server: NEG-Server
x-server-id: 102
Content-Length: 395
Accept-Ranges: bytes
Date: Mon, 24 Jun 2013 08:40:40 GMT
Age: 0
Connection: keep-alive
X-Served-By: E408
X-Ver: 13012401
X-Source-IP: ###
X-client-IP: ###
X-Cache: MISS
X-Cache-Hits: 0
```

### Response Body
```JSON
[
	{
		"Title": "Computer Hardware",
		"StoreDepa": "ComputerHardware",
		"StoreID": 1,
		"ShowSeeAllDeals": true
	},
	{
		"Title": "PCs & Laptops",
		"StoreDepa": "PCNotebook",
		"StoreID": 3,
		"ShowSeeAllDeals": true
	},
	...
]
```

## Store Categories Menu
After selecting a store, categories of the store may be viewed by browsing to `/Stores.egg/Categories/{StoreID}/`


### Request
```
GET /Stores.egg/Categories/1/ HTTP/1.1
Host: www.ows.newegg.com
Accept-Language: en-us
Pragma: no-cache
User-Agent: Newegg iPhone App / 3.1.2
X-ThirdParty-UTMA: ###
X-HighResolution: true
Accept: */*
MobileVisitor: ###
Connection: keep-alive
X-Signature: ###
Cookie: ###
Connection: keep-alive
X-Timestamp: 1372063245.255948
Accept-Encoding: gzip, deflate
```

### Response
```
HTTP/1.1 200 OK
Cache-Control: private
Content-Type: application/json; charset=utf-8
Vary: Accept-Encoding
Server: Microsoft-IIS/7.5
X-AspNetMvc-Version: 1.0
X-AspNet-Version: 2.0.50727
Set-Cookie: ###
Server: NEG-Server
x-server-id: 122
Content-Length: 2717
Accept-Ranges: bytes
Date: Mon, 24 Jun 2013 08:40:46 GMT
Age: 0
Connection: keep-alive
X-Served-By: E408
X-Ver: 13012401
X-Source-IP: ###
X-client-IP: ###
X-Cache: MISS
X-Cache-Hits: 0
```

### Response Body
```JSON
[
	{
		"Description": "Backup Devices & Media",
		"CategoryType": 0,
		"CategoryID": 2,
		"StoreID": 1,
		"ShowSeeAllDeals": true,
		"NodeId": 6642
	},
	...
	{
		"Description": "CPUs / Processors",
		"CategoryType": 0,
		"CategoryID": 34,
		"StoreID": 1,
		"ShowSeeAllDeals": true,
		"NodeId": 6676
	},
	...
]
```

## Category Sub-Category Menu
To view sub-categories of a store category browse to: `/Stores.egg/Navigation/{StoreID}/{CategoryID}/{NodeId}/`

### Request
```
GET /Stores.egg/Navigation/1/34/6676/ HTTP/1.1
Host: www.ows.newegg.com
Accept-Language: en-us
Pragma: no-cache
User-Agent: Newegg iPhone App / 3.1.2
X-ThirdParty-UTMA: 1362554180.1363017685.1372063245.1372063246.285
X-HighResolution: true
Accept: */*
MobileVisitor: ###
Connection: keep-alive
X-Signature: /eSdVuS4JgZw7Oovwirboj1+UBU=
Cookie: VisitorID=50121372063245166192611
Connection: keep-alive
X-Timestamp: 1372063248.103329
Accept-Encoding: gzip, deflate
```

### Response
```
HTTP/1.1 200 OK
Cache-Control: private
Content-Type: application/json; charset=utf-8
Vary: Accept-Encoding
Server: Microsoft-IIS/7.5
X-AspNetMvc-Version: 1.0
X-AspNet-Version: 2.0.50727
Set-Cookie: ###
Server: NEG-Server
x-server-id: 124
Content-Length: 740
Accept-Ranges: bytes
Date: Mon, 24 Jun 2013 08:40:48 GMT
Age: 0
Connection: keep-alive
X-Served-By: E408
X-Ver: 13012401
X-Source-IP: ###
X-client-IP: ###
X-Cache: MISS
X-Cache-Hits: 0
```

### Response Body
```JSON
[
	{
		"Description": "Processors - Desktops",
		"CategoryType": 1,
		"CategoryID": 343,
		"StoreID": 1,
		"ShowSeeAllDeals": false,
		"NodeId": 7671
	},
	{
		"Description": "Processors - Servers",
		"CategoryType": 1,
		"CategoryID": 727,
		"StoreID": 1,
		"ShowSeeAllDeals": false,
		"NodeId": 8494
	},
	...
]
```