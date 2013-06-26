# Filtering
## Guided Search
Filtering using guided search allows the user to select a single item from each filtering category. The list of available filters itself is filtered as you select more filters. The value on which the filters are discriminated is the `NValue` field `NavigationContentList > NavigationItemList > NValue`. `NValue` consists of a unique set of space-separated list of integers per item. Some `NValue`s are used as prefixes to determine if a filter should be displayed or not based on an existing set of selected filters.

For example an unfiltered search for items in `Computer Hardware` > `CPUs / Processors` > `Processors - Desktops` would have a request body of the following:

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

As you can see `NValue` is empty indicating no filters have been applied. To apply a price filter select the `NValue` from the `NavigationContentList` for the desired price range (unnecessary fields have been elided from the following data):

```JSON
{
	"NavigationContentList": [
		...,
		{
			"TitleItem": {
				"Description": "Price",
				"ItemCount": 0,
				"NValue": "4015",
				"ElementValue": "4015"
			},
			"NavigationItemList": [
				{
					"Description": "$25 - $50",
					"NValue": "100007671 4025",
					"ElementValue": "4025"
				},
				{
					"Description": "$50 - $75",
					"NValue": "100007671 4026",
					"ElementValue": "4026"
				},
				{
					"Description": "$75 - $100",
					"NValue": "100007671 4027",
					"ElementValue": "4027"
				},
				...
			]
		},
		...
	]
}
```

In the following example the processors are filtered by those falling into the `$50 - $75` category. The `NavigationContentList` of the response includes a list of filters, omitting those which would produce no results or categories which already have a filter selected. The effect is that only a single filter per category may be applied in guided search.

```JSON
{
	"PageNumber": 1,
	"BrandId": -1,
	"NValue": "100007671 4026 ",
	"StoreDepaId": 1,
	"NodeId": -1,
	"Keyword": "",
	"IsSubCategorySearch": false,
	"SubCategoryId": -1,
	"Sort": "FEATURED",
	"CategoryId": -1,
	"IsUPCCodeSearch": false
}
```

The available filters given in the response are as follows:
```JSON
{
	"NavigationContentList": [
		...
		{
			"TitleItem": {
				"Description": "Series",
				"ItemCount": 0,
				"NValue": "600005532",
				"ElementValue": "600005532"
			},
			"NavigationItemList": [
				{
					"Description": "Celeron",
					"NValue": "100007671 50001157 4026 600005539",
					"ElementValue": "600005539"
				},
				{
					"Description": "Core 2 Duo",
					"NValue": "100007671 50001157 4026 600005560",
					"ElementValue": "600005560"
				},
				{
					"Description": "Pentium",
					"NValue": "100007671 50001157 4026 600005583",
					"ElementValue": "600005583"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "CPU Socket Type",
				"ItemCount": 0,
				"NValue": "600005840",
				"ElementValue": "600005840"
			},
			"NavigationItemList": [
				{
					"Description": "LGA 775",
					"NValue": "100007671 50001157 4026 600005851",
					"ElementValue": "600005851"
				},
				{
					"Description": "LGA 1155",
					"NValue": "100007671 50001157 4026 600095610",
					"ElementValue": "600095610"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "Core",
				"ItemCount": 0,
				"NValue": "600005587",
				"ElementValue": "600005587"
			},
			"NavigationItemList": [
				{
					"Description": "Ivy Bridge",
					"NValue": "100007671 50001157 4026 600315409",
					"ElementValue": "600315409"
				},
				{
					"Description": "Sandy Bridge",
					"NValue": "100007671 50001157 4026 600095611",
					"ElementValue": "600095611"
				},
				{
					"Description": "Wolfdale",
					"NValue": "100007671 50001157 4026 600005665",
					"ElementValue": "600005665"
				}
			]
		},
		...
	]
}
```

To apply a second filter limiting the search to only `Intel` processors, the set of integers in `NValue` would be updated to include `100007671 50001157` which would produce the following request body:

```JSON
{
	"PageNumber": 1,
	"BrandId": -1,
	"NValue": "50001157 100007671 4026 ",
	"StoreDepaId": 1,
	"NodeId": -1,
	"Keyword": "",
	"IsSubCategorySearch": false,
	"SubCategoryId": -1,
	"Sort": "FEATURED",
	"CategoryId": -1,
	"IsUPCCodeSearch": false
}
```

To my knowledge the `NValue` list is unordered.

## Power Search Filters
Power searching requires a series of requests. The first of which returns a description of all filter categories and possible values for each filter. The following example is the list of available filters for `Computer Hardware` > `CPUs / Processors` > `Processors - Desktops`.
### Request
```
GET /PowerSearchContent.egg/0/343/-1/
```

### Response
```JSON
{
	"PageTitle": "Power Search: Processors - Desktops",
	"CoremetricsInfo": {
		"CategoryID": "ProductPowerSearch",
		"ProductName": "",
		"PageID": "ProductPowerSearch",
		"Brand": ""
	},
	"PowerSearchOptions": [
		...,
		{
			"TitleItem": {
				"IsSelected": false,
				"TId": 0,
				"TitleText": "",
				"ElementName": "",
				"Description": "Multi-Core",
				"StoreID": 0,
				"CustomLink": "",
				"ElementValue": "",
				"BrandId": 0,
				"CategoryId": 0,
				"DepaId": 0,
				"SubCategoryId": 0
			},
			"Items": [
				{
					"ElementName": "",
					"ElementValue": "",
					"Description": "Any",
					"StoreID": 0,
					"CustomLink": "",
					"IsSelected": true,
					"SubCategoryId": 0,
					"TitleText": "",
					"BrandId": 0,
					"CategoryId": 0,
					"DepaId": 0,
					"TId": 0
				},
				{
					"ElementName": "PropertyCodeValue",
					"ElementValue": "3028:20276",
					"Description": "Single-Core",
					"StoreID": 0,
					"CustomLink": "",
					"IsSelected": false,
					"SubCategoryId": 0,
					"TitleText": "",
					"BrandId": 0,
					"CategoryId": 0,
					"DepaId": 0,
					"TId": 0
				},
				{
					"ElementName": "PropertyCodeValue",
					"ElementValue": "3028:20275",
					"Description": "Dual-Core",
					"StoreID": 0,
					"CustomLink": "",
					"IsSelected": false,
					"SubCategoryId": 0,
					"TitleText": "",
					"BrandId": 0,
					"CategoryId": 0,
					"DepaId": 0,
					"TId": 0
				},
				{
					"ElementName": "PropertyCodeValue",
					"ElementValue": "3028:34507",
					"Description": "Triple-Core",
					"StoreID": 0,
					"CustomLink": "",
					"IsSelected": false,
					"SubCategoryId": 0,
					"TitleText": "",
					"BrandId": 0,
					"CategoryId": 0,
					"DepaId": 0,
					"TId": 0
				},
				{
					"ElementName": "PropertyCodeValue",
					"ElementValue": "3028:25342",
					"Description": "Quad-Core",
					"StoreID": 0,
					"CustomLink": "",
					"IsSelected": false,
					"SubCategoryId": 0,
					"TitleText": "",
					"BrandId": 0,
					"CategoryId": 0,
					"DepaId": 0,
					"TId": 0
				},
				{
					"ElementName": "PropertyCodeValue",
					"ElementValue": "3028:55196",
					"Description": "Six-Core",
					"StoreID": 0,
					"CustomLink": "",
					"IsSelected": false,
					"SubCategoryId": 0,
					"TitleText": "",
					"BrandId": 0,
					"CategoryId": 0,
					"DepaId": 0,
					"TId": 0
				},
				{
					"ElementName": "PropertyCodeValue",
					"ElementValue": "3028:193801",
					"Description": "Eight-Core",
					"StoreID": 0,
					"CustomLink": "",
					"IsSelected": false,
					"SubCategoryId": 0,
					"TitleText": "",
					"BrandId": 0,
					"CategoryId": 0,
					"DepaId": 0,
					"TId": 0
				}
			]
		},
		...
	]
}
```

## Power Search
### Single Filter
To search using a particular filter the `ElementValue` must be split on the `:` and added to the `SearchProperies` list in the request body. For example searching for quad-core processors can be done using the following request:

### Request
```
POST /PowerSearch.egg
```

### Request Body
The `ElementValue` for quad-core processors is `3028:25342`.
```JSON
{
	"PageNumber": 1,
	"ProductType": [],
	"SearchProperties": [
		{
			"PropertyId": "3028",
			"ValueId": "25342"
		}
	],
	"MinPrice": "",
	"NValues": "100007671",
	"SrchInDesc": "",
	"BrandList": [],
	"MaxPrice": ""
}
```

### Response
See Searching.

### Multiple Filters
Searching with multiple filters in the same category is done by appending multiple filters to the `SearchProperties` list. The following example searches for quad-, hexa- and octo-core processors.
```JSON
{
	"PageNumber": 1,
	"ProductType": [],
	"SearchProperties": [
		{
			"PropertyId": "3028",
			"ValueId": "25342"
		},
		{
			"PropertyId": "3028",
			"ValueId": "55196"
		},
		{
			"PropertyId": "3028",
			"ValueId": "193801"
		}
	],
	"MinPrice": "",
	"NValues": "100007671",
	"SrchInDesc": "",
	"BrandList": [],
	"MaxPrice": ""
}
```

### Exceptions
 * The `NValue` field appears to be populated using data from the response to the `/Search.egg/Advanced/` request.
 * Filtering on `ProductType` appends the `ElementValue` to the `ProductType` field instead of `SearchProperties`.
 * Filtering on manufacturer appends the `ElementValue` to the `BrandList` field instead of `SearchProperties`.
 * `MinPrice` and `MaxPrice` fields don't appear to be used by the iPhone application, despite being present in all power search request bodies.