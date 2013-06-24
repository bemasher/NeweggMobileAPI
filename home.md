# Home Page
## Shopping Guide
Starting in the home tab, a list of stores are populated as buttons at the bottom of the screen. These include stores like: Electronic, PC Showcase and Build Your Own. The iPhone app does not appear to make use of the `Description` or `BannerImage` fields in each of the `ShoppingGuide` objects.
### Request
```
GET /Configurations.egg/ShoppingGuideConfig HTTP/1.1
Host: www.ows.newegg.com
User-Agent: Newegg iPhone App / 3.1.2
Accept: */*
Accept-Encoding: gzip, deflate
Accept-Language: en-us
Connection: keep-alive
Cookie: ###
Mobilevisitor: VERSIONINFO=iPhone App 3.1.2
X-Highresolution: true
X-Signature: ###
X-Timestamp: 1371995642.144446
```
### Response
```
HTTP/1.1 200 OK
Content-Length: 689
Accept-Ranges: bytes
Age: 0
Cache-Control: private
Connection: keep-alive
Content-Encoding: gzip
Content-Type: application/json; charset=utf-8
Date: Sun, 23 Jun 2013 13:50:47 GMT
Server: Microsoft-IIS/7.5
Server: NEG-Server
Set-Cookie: ***;
Vary: Accept-Encoding
X-Aspnet-Version: 2.0.50727
X-Aspnetmvc-Version: 1.0
X-Cache: MISS
X-Cache-Hits: 0
X-Served-By: E313
X-Server-Id: 14
X-Ver: 13012401
```

### Response Body
```JSON
{
	"Enable": true,
	"ShoppingGuideList": [
		{
			"Enable": true,
			"DataAccessMethod": "store",
			"Title": "Electronic...",
			"Description": "Redefine Viewing",
			"BannerImage": "http://promotions.newegg.com/homepage/Pillar/060911/redefine.jpg",
			"PageId": "tab:{Electronic}",
			"CategoryId": "IPD2102640000",
			"Store": {
				"StoreType": 1,
				"StoreId": 1,
				"CategoryId": 264,
				"IncludeFeaturedItem": false
			},
			"XmlData": {
				"XmlFileName": "ShoppingGuideItems_1_USA_EN",
				"PageSize": 20
			},
			"Search": {
				"NValue": "",
				"IsSubCategorySearch": false,
				"SubCategoryId": -1,
				"BrandId": -1,
				"StoreDepaId": -1,
				"CategoryId": -1,
				"IsUPCCodeSearch": false,
				"NodeId": -1,
				"Sort": "",
				"IsComboBundle": false
			}
		},
		...
	]
}
```

## Spotlight
The spotlight is a single featured item. This item shares the same format for items obtained through searches which are covered later in this document.

### Request
```
GET /Promotions.egg/Spotlight HTTP/1.1
Host: www.ows.newegg.com
User-Agent: Newegg iPhone App / 3.1.2
Accept: */*
Accept-Encoding: gzip, deflate
Accept-Language: en-us
Connection: keep-alive
Cookie: ###
Mobilevisitor: VERSIONINFO=iPhone App 3.1.2
X-Highresolution: true
X-Signature: ###
X-Timestamp: 1371995642.143917
```

### Response
```
HTTP/1.1 200 OK
Content-Length: 682
Accept-Ranges: bytes
Age: 0
Cache-Control: private
Connection: keep-alive
Content-Encoding: gzip
Content-Type: application/json; charset=utf-8
Date: Sun, 23 Jun 2013 13:50:47 GMT
Server: Microsoft-IIS/7.5
Server: NEG-Server
Set-Cookie: ###
Vary: Accept-Encoding
X-Aspnet-Version: 2.0.50727
X-Aspnetmvc-Version: 1.0
X-Cache: MISS
X-Cache-Hits: 0
X-Served-By: E313
X-Server-Id: 13
X-Ver: 13012401
```

### Response Body
```JSON
{
	"ItemNumber": "9SIA04M0CN1405",
	"OriginalPrice": "$79.99",
	"IsShowOriginalPrice": true,
	"IsShowAfterRebate": false,
	"AfterRebateText": null,
	"FinalPrice": "$49.94",
	"ProductTitle": "New Balance MW950 Men's Leather Running Shoes ",
	"PercentOff": "38%",
	"LogoImageUrl": "http://promotions.newegg.com/AppWorld/Mobile/iPad/deal_1.png",
	"IsHot": false,
	"StoreLink": "http://www.newegg.com/Store/SubCategory.aspx?SubCategory=2787&amp;name=Shoes&amp;cm_sp=Spotlight-_-adlink-_-06232013",
	"StoreTitle": "shop Shoes",
	"IsRegularCombo": false,
	"IsCombo": 0,
	"ComboImages": null,
	"ProductImageUrl": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll300/A04M_1_20130328140763743.jpg",
	"ProductImages": [
		{
			"ItemNumber": null,
			"Title": null,
			"FullPath": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll300/A04M_1_20130328140763743.jpg",
			"ThumbnailImagePath": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll125/A04M_1_20130328140763743.jpg",
			"SmallImagePath": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll200/A04M_1_20130328140763743.jpg",
			"PathSize35": "http://images10.newegg.com/ProductImageCompressAll100/A04M_1_20130328140763743.jpg",
			"PathSize60": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll125/A04M_1_20130328140763743.jpg",
			"PathSize100": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll200/A04M_1_20130328140763743.jpg",
			"PathSize125": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll200/A04M_1_20130328140763743.jpg",
			"PathSize180": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll300/A04M_1_20130328140763743.jpg",
			"PathSize300": "http://images10.newegg.com/NeweggImage/productimage/A04M_1_20130328140763743.jpg",
			"PathSize640": "http://images10.newegg.com/NeweggImage/productimage/A04M_1_20130328140763743.jpg"
		}
	]
}
```

## Shell Shockers
Shell shockers are shown as an automatically rotating list of shell shocker items. These items share many of the same fields as those obtained through search results, with a few extras relating to the current deal like stock and total discount.

### Request
```
GET /Promotions.egg/ShellShockers HTTP/1.1
Host: www.ows.newegg.com
User-Agent: Newegg iPhone App / 3.1.2
Accept: */*
Accept-Encoding: gzip, deflate
Accept-Language: en-us
Connection: keep-alive
Cookie: ###
Mobilevisitor: VERSIONINFO=iPhone App 3.1.2
X-Highresolution: true
X-Signature: ###
X-Timestamp: 1371995642.143389
```

### Response
```
HTTP/1.1 200 OK
Content-Length: 1019
Accept-Ranges: bytes
Age: 0
Cache-Control: private
Connection: keep-alive
Content-Encoding: gzip
Content-Type: application/json; charset=utf-8
Date: Sun, 23 Jun 2013 13:50:47 GMT
Server: Microsoft-IIS/7.5
Server: NEG-Server
Set-Cookie: ###
Vary: Accept-Encoding
X-Aspnet-Version: 2.0.50727
X-Aspnetmvc-Version: 1.0
X-Cache: MISS
X-Cache-Hits: 0
X-Served-By: E313
X-Server-Id: 12
X-Ver: 13012401
```

### Response Body
```JSON
[
	{
		"IsSoldout": false,
		"OriginalPrice": "$123.98",
		"FinalPrice": "$74.99",
		"IsShowOriginalPrice": true,
		"ShellShockItemNumber": "1352254",
		"ShellShockerItemType": 1,
		"ShellShockerStatusType": 2,
		"UpComingDeal": null,
		"UpComingTime": null,
		"CurrentTimeZone": null,
		"ProductTitle": "Rosewill Articulating 37\" - 65\" Full Motion ...",
		"IsShowDiscountPercent": false,
		"DiscountPercent": null,
		"AfterRebate": null,
		"IsShowAfterRebate": false,
		"ShellShockerImages": [
			{
				"Title": null,
				"FullPath": "http://images17.newegg.com/is/image/newegg/82-021-103-TS?$S180$",
				"ThumbnailImagePath": "http://images17.newegg.com/is/image/newegg/82-021-103-TS?$S60$",
				"SmallImagePath": "http://images17.newegg.com/is/image/newegg/82-021-103-TS?$S125$",
				"PathSize35": "http://images17.newegg.com/is/image/newegg/82-021-103-TS?$S35$",
				"PathSize60": "http://images17.newegg.com/is/image/newegg/82-021-103-TS?$S60$",
				"PathSize100": "http://images17.newegg.com/is/image/newegg/82-021-103-TS?$S100$",
				"PathSize125": "http://images17.newegg.com/is/image/newegg/82-021-103-TS?$S125$",
				"PathSize180": "http://images17.newegg.com/is/image/newegg/82-021-103-TS?$S180$",
				"PathSize300": "http://images17.newegg.com/is/image/newegg/82-021-103-TS?$S300$",
				"PathSize640": "http://images17.newegg.com/is/image/newegg/82-021-103-TS?$S640$"
			},
			{
				"Title": null,
				"FullPath": "http://images17.newegg.com/is/image/newegg/82-021-128-TS?$S180$",
				"ThumbnailImagePath": "http://images17.newegg.com/is/image/newegg/82-021-128-TS?$S60$",
				"SmallImagePath": "http://images17.newegg.com/is/image/newegg/82-021-128-TS?$S125$",
				"PathSize35": "http://images17.newegg.com/is/image/newegg/82-021-128-TS?$S35$",
				"PathSize60": "http://images17.newegg.com/is/image/newegg/82-021-128-TS?$S60$",
				"PathSize100": "http://images17.newegg.com/is/image/newegg/82-021-128-TS?$S100$",
				"PathSize125": "http://images17.newegg.com/is/image/newegg/82-021-128-TS?$S125$",
				"PathSize180": "http://images17.newegg.com/is/image/newegg/82-021-128-TS?$S180$",
				"PathSize300": "http://images17.newegg.com/is/image/newegg/82-021-128-TS?$S300$",
				"PathSize640": "http://images17.newegg.com/is/image/newegg/82-021-128-TS?$S640$"
			}
		],
		"IsWhatsHot": false,
		"IsHot": false
	},
	...
]
```

## Activity
The purpose of this request is unknown.

### Request
```
GET /Promotions.egg/Activity HTTP/1.1
Host: www.ows.newegg.com
User-Agent: Newegg iPhone App / 3.1.2
Accept: */*
Accept-Encoding: gzip, deflate
Accept-Language: en-us
Connection: keep-alive
Cookie: ###
Mobilevisitor: VERSIONINFO=iPhone App 3.1.2
X-Highresolution: true
X-Signature: ###
X-Timestamp: 1371995642.142075
```

### Response
```
HTTP/1.1 200 OK
Accept-Ranges: bytes
Age: 0
Cache-Control: private
Connection: keep-alive
Date: Sun, 23 Jun 2013 13:50:47 GMT
Server: Microsoft-IIS/7.5
Server: NEG-Server
Set-Cookie: ###
X-Aspnet-Version: 2.0.50727
X-Aspnetmvc-Version: 1.0
X-Cache: MISS
X-Cache-Hits: 0
X-Served-By: E313
X-Server-Id: 04
X-Ver: 13012401
```

## iPhone Client
This request appears to be used provide default settings to the app. There are options which indicate support for certain features like push notifications, barcode scanning and links to download updated versions of the app.

### Request
```
GET /Configuration.egg/IphoneClient HTTP/1.1
Host: www.ows.newegg.com
User-Agent: Newegg iPhone App / 3.1.2
Accept: */*
Accept-Encoding: gzip, deflate
Accept-Language: en-us
Connection: keep-alive
Cookie: ###
Mobilevisitor: VERSIONINFO=iPhone App 3.1.2
X-Highresolution: true
X-Signature: ###
X-Timestamp: 1371995641.337552
```

### Response
```
HTTP/1.1 200 OK
Content-Length: 859
Accept-Ranges: bytes
Age: 0
Cache-Control: private
Connection: keep-alive
Content-Encoding: gzip
Content-Type: application/json; charset=utf-8
Date: Sun, 23 Jun 2013 13:50:46 GMT
Server: Microsoft-IIS/7.5
Server: NEG-Server
Vary: Accept-Encoding
X-Aspnet-Version: 2.0.50727
X-Aspnetmvc-Version: 1.0
X-Cache: MISS
X-Cache-Hits: 0
X-Served-By: E313
X-Server-Id: 24
X-Ver: 13012401
```

### Response Body
```JSON
{
	"ServiceHost": {
		"Name": "E3WEB24"
	},
	"VersionControl": {
		"DeviceType": 0,
		"ClientVersion": "3.1.2",
		"PayPal": {
			"Enable": true
		},
		"PushNotification": {
			"Enable": true
		},
		"Activity": {
			"Enable": true
		},
		"AvailableVersions": [
			"3.1.1",
			"3.1.0",
			"3.0.7"
		],
		"AppStoreURL": "http://phobos.apple.com/WebObjects/MZStore.woa/wa/viewSoftware?id=345188269&cc=us&mt=8&uo=6",
		"Description": "\n      <strong>We have newest version on App store. Please upgrade it to take advantage of the new features and performance improvement.</strong><br>\n      <ul>\n                <li>- Add Power Search.</li>\n                 <li>- Bug fixes.</li>\n       </ul>\n      ",
		"Key": 0,
		"TimeMachine": {
			"Enabled": false,
			"Url": "http://promotions.newegg.com/AppWorld/Mobile/Service/timemachine/banner/phone.png"
		},
		"Welcomescreen": {
			"Enabled": false,
			"Url": "http://www.newegg.com"
		},
		"ThirdPartyPayment": []
	},
	"ImageCaching": {
		"Enabled": true,
		"MaxPixelCountExpression": "480*320*10",
		"MaxPixelCount": 1536000
	},
	"Cormetrics": {
		"Enabled": true,
		"ClientID": "90172959",
		"RequestServer": {
			"HttpServer": "http://data.coremetrics.com/eluminate?",
			"HttpsServer": "https://data.coremetrics.com/eluminate?"
		},
		"Vn1": "4.0.23",
		"Vn2": "e4.0"
	},
	"BarcodeScan": {
		"Enable": true
	},
	"ContactUs": null
}
```
