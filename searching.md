# Searching
## Keyword Search
The requests sends a JSON structure indicating a keyword search and a starting page number. The response returns a JSON structure including a menu and items returned by the search. These will be broken into sections and explained.

### Request
```
POST /Search.egg/Advanced/
Content-Type: application/x-www-form-urlencoded
```

### Request Body
```JSON
{
	"PageNumber": 1,
	"BrandId": -1,
	"NValue": "",
	"StoreDepaId": -1,
	"NodeId": -1,
	"Keyword": "haswell 4770k",
	"IsSubCategorySearch": false,
	"SubCategoryId": -1,
	"Sort": "FEATURED",
	"CategoryId": -1,
	"IsUPCCodeSearch": false
}
```

### Response
See [Search Results](#search-results).

## Searching by Category
To view items belonging to a category. The following maps fields of a sub-category to fields of the request body. See Browsing for more information on these fields.

<table>
	<tr><th>Request Field</th><th>Sub-Category Menu Fields</th></tr>
	<tr><td>StoreID</td><td>StoreDepaId</td></tr>
	<tr><td>NodeId</td><td>NodeId</td></tr>
	<tr><td>CategoryID</td><td>SubCategoryId</td></tr>
</table>

### Request
```
POST /Search.egg/Advanced/
Content-Type: application/x-www-form-urlencoded
```

### Request body
```JSON
{
	"PageNumber": 1,
	"BrandId": -1,
	"NValue": "",
	"StoreDepaId": 1,
	"NodeId": 7671,
	"Keyword": "",
	"IsSubCategorySearch": true,
	"SubCategoryId": 343,
	"Sort": "FEATURED",
	"CategoryId": -1,
	"IsUPCCodeSearch": false
}
```

### Response
See [Search Results](#search-results).

## Auto Completion
When selecting the search button a search prompt is brought up which performs auto completion as the user types, these responses are presented as a list of keywords which perform keyword search. `ProductItemCount` never appears to be populated.

### Request
```
GET http://www.ows.newegg.com/AutoKeywords.egg/?keyword=haswell HTTP/1.1
```

### Response
```JSON
[
	{
		"Keyword": "haswell processor",
		"ProductItemCount": 0
	},
	{
		"Keyword": "haswell intel",
		"ProductItemCount": 0
	},
	...
]
```

## Search Results
The `NavigationContentList` consists of a list of menu items. The `TitleItem` in each is presented as a clickable button which brings up a list of subcategories defined by items in `NavigationItemList`.
```JSON
{
	"NavigationContentList": [
		{
			"TitleItem": {
				"Description": "Useful Links",
				"ItemCount": 0,
				"StoreDepaId": -1,
				"StoreType": -2,
				"CategoryId": -1,
				"SubCategoryId": -1,
				"BrandId": -1,
				"NValue": "4800",
				"ElementValue": "4800",
				"CategoryDescription": null
			},
			"NavigationItemList": [
				{
					"Description": "ShopRunner Eligible",
					"ItemCount": 73,
					"StoreDepaId": -1,
					"StoreType": -1,
					"CategoryId": -1,
					"SubCategoryId": -1,
					"BrandId": -1,
					"NValue": "4815",
					"ElementValue": "4815",
					"CategoryDescription": null
				},
				{
					"Description": "Free Shipping",
					"ItemCount": 33,
					"StoreDepaId": 94,
					"StoreType": 4,
					"CategoryId": -1,
					"SubCategoryId": -1,
					"BrandId": -1,
					"NValue": "4808",
					"ElementValue": "4808",
					"CategoryDescription": null
				},
				...
			]
		},
		{
			"TitleItem": {
				"Description": "Price",
				"ItemCount": 0,
				"StoreDepaId": -1,
				"StoreType": -2,
				"CategoryId": -1,
				"SubCategoryId": -1,
				"BrandId": -1,
				"NValue": "4015",
				"ElementValue": "4015",
				"CategoryDescription": null
			},
			"NavigationItemList": [
				{
					"Description": "$50 - $75",
					"ItemCount": 7,
					"StoreDepaId": -1,
					"StoreType": -1,
					"CategoryId": -1,
					"SubCategoryId": -1,
					"BrandId": -1,
					"NValue": "4026",
					"ElementValue": "4026",
					"CategoryDescription": null
				},
				{
					"Description": "$75 - $100",
					"ItemCount": 17,
					"StoreDepaId": -1,
					"StoreType": -1,
					"CategoryId": -1,
					"SubCategoryId": -1,
					"BrandId": -1,
					"NValue": "4027",
					"ElementValue": "4027",
					"CategoryDescription": null
				},
				...
			]
		},
		...
	],
```

The following are keys at the top level of the response body.
```JSON
	"RelatedLinkList": null,
	"CoremetricsInfo": {
		"CategoryID": "H10",
		"ProductName": null,
		"PageID": "search results: successful",
		"Brand": null
	},
	"IsAllComboBundle": false,
	"CanBeCompare": false,
	"MasterComboStoreId": -1,
	"SubCategoryId": -1,
	"HasDeactivatedItems": false,
	"HasHasSimilarItems": false,
	"SearchProvider": 0,
	"SearchResultType": 1,
	"CanPowerSearch": false,
```

The largest portion of the response body is dedicated to `ProductListItems` which are fixed links to items and include information like price, description, images and the like.
```JSON
	"ProductListItems": [
		{
			"IsCellPhoneItem": false,
			"ShowOriginalPrice": false,
			"MailInRebateText": "",
			"IsComboBundle": false,
			"ProductStockType": 0,
			"MappingFinalPrice": null,
			"IsFeaturedItem": false,
			"IsMicrosoftDownloadItem": false,
			"IsProductKeyOnly": false,
			"Title": "Intel Core i7-4770K Haswell 3.5GHz LGA 1150 84W Quad-Core Desktop Processor Intel HD Graphics BX80646I74770K",
			"OriginalPrice": "$349.99",
			"Discount": null,
			"FinalPrice": "$349.99",
			"FreeShippingFlag": true,
			"Model": "BX80646I74770K",
			"ReviewSummary": {
				"Rating": 5,
				"TotalReviews": "[31]"
			},
			"Image": {
				"ItemNumber": null,
				"Title": null,
				"FullPath": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S180W$",
				"ThumbnailImagePath": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S125W$",
				"SmallImagePath": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S180W$",
				"PathSize35": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S100$",
				"PathSize60": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S125W$",
				"PathSize100": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S180W$",
				"PathSize125": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S180W$",
				"PathSize180": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S300W$",
				"PathSize300": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S640W$",
				"PathSize640": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S640W$"
			},
			"SellerName": null,
			"ParentItem": null,
			"SellerId": null,
			"ShipByNewegg": 0,
			"ItemGroupID": 0,
			"ItemOwnerType": 0,
			"NumberOfReviews": 0,
			"AverageRating": 0,
			"Instock": true,
			"XmlSpec": null,
			"WarrantyInfo": null,
			"NeweggItemNumber": "N82E16819116901",
			"PromotionInfo": "Free Skull T-Shirt & $15 gift card w/ purchase, limited offer",
			"InstockForCombo": true,
			"ETA": "/Date(-62135568000000)/",
			"IsInPMCC": false,
			"CanAddToCart": false,
			"StrCartImg": null,
			"StrAlt": null,
			"StrAddItem": null,
			"StaticText": null,
			"InstantSaving": 0,
			"HasMappingPrice": false,
			"UnitPrice": 0,
			"BrandInfo": null,
			"LimitQuantity": 0,
			"IsShellShockerItem": false,
			"PromotionText": "Free Skull T-Shirt & $15 gift card w/ purchase, limited offer",
			"ItemMapPriceMarkType": 0,
			"IsHot": false,
			"IsPreLaunch": false,
			"ItemNumber": "19-116-901",
			"Academic": false
		},
		...
	],
```

`PaginationInfo` provides information in various requests about how many items are displayed per page and how many total items a search produced. `PageCount` never seems to be populated with anything other than 0.
```JSON
	"PaginationInfo": {
		"TotalCount": 78,
		"PageSize": 20,
		"PageNumber": 1,
		"PageCount": 0,
		"PageNumberList": null
	}
}
```

## Sorting
Sorting results is done by setting the `Sort` field of the request body to one of the following values. Defaults to `FEATURED`.

<table>
	<tr><th>Value</th><th>Description</th></tr>
	<tr><td>FEATURED</td><td>Featured Items</tr>
	<tr><td>RATING</td><td>Best Rating</tr>
	<tr><td>PRICE</td><td>Lowest Price</tr>
	<tr><td>PRICED</td><td>Highest Price</tr>
	<tr><td>REVIEWS</td><td>Most Reviews</tr>
</table>