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

In the following example the processors are filtered by those falling into the `$50 - $75` category. The `NavigationContentList` of the response includes a list of filters omitting filters which would produce no results or categories which already have a filter selected. The effect is that only a single filter per category may be applied in guided search.

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
				"Description": "Useful Links",
				"ItemCount": 0,
				"NValue": "4800",
				"ElementValue": "4800"
			},
			"NavigationItemList": [
				{
					"Description": "Free Shipping",
					"NValue": "100007671 50001157 4026 4808",
					"ElementValue": "4808"
				},
				{
					"Description": "ShopRunner Eligible",
					"NValue": "100007671 50001157 4026 4815",
					"ElementValue": "4815"
				},
				{
					"Description": "Discount Item",
					"NValue": "100007671 50001157 4026 4803",
					"ElementValue": "4803"
				},
				{
					"Description": "Refurbished",
					"NValue": "100007671 50001157 4026 4016",
					"ElementValue": "4016"
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
		{
			"TitleItem": {
				"Description": "Operating Frequency",
				"ItemCount": 0,
				"NValue": "600005681",
				"ElementValue": "600005681"
			},
			"NavigationItemList": [
				{
					"Description": "2.5GHz - 2.99GHz",
					"NValue": "100007671 50001157 4026 600005685",
					"ElementValue": "600005685"
				},
				{
					"Description": "3.0GHz and higher",
					"NValue": "100007671 50001157 4026 600005686",
					"ElementValue": "600005686"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "FSB",
				"ItemCount": 0,
				"NValue": "600005754",
				"ElementValue": "600005754"
			},
			"NavigationItemList": [
				{
					"Description": "1066MHz",
					"NValue": "100007671 50001157 4026 600005761",
					"ElementValue": "600005761"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "L2 Cache",
				"ItemCount": 0,
				"NValue": "600005782",
				"ElementValue": "600005782"
			},
			"NavigationItemList": [
				{
					"Description": "3MB",
					"NValue": "100007671 50001157 4026 600005801",
					"ElementValue": "600005801"
				},
				{
					"Description": "2 x 256KB",
					"NValue": "100007671 50001157 4026 600005792",
					"ElementValue": "600005792"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "L3 Cache",
				"ItemCount": 0,
				"NValue": "600005808",
				"ElementValue": "600005808"
			},
			"NavigationItemList": [
				{
					"Description": "2MB",
					"NValue": "100007671 50001157 4026 600005811",
					"ElementValue": "600005811"
				},
				{
					"Description": "3MB",
					"NValue": "100007671 50001157 4026 600005816",
					"ElementValue": "600005816"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "Manufacturing Tech",
				"ItemCount": 0,
				"NValue": "600005818",
				"ElementValue": "600005818"
			},
			"NavigationItemList": [
				{
					"Description": "45 nm",
					"NValue": "100007671 50001157 4026 600005824",
					"ElementValue": "600005824"
				},
				{
					"Description": "32 nm",
					"NValue": "100007671 50001157 4026 600005825",
					"ElementValue": "600005825"
				},
				{
					"Description": "22 nm",
					"NValue": "100007671 50001157 4026 600315411",
					"ElementValue": "600315411"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "Hyper-Threading Support",
				"ItemCount": 0,
				"NValue": "600000350",
				"ElementValue": "600000350"
			},
			"NavigationItemList": [
				{
					"Description": "No",
					"NValue": "100007671 50001157 4026 600000352",
					"ElementValue": "600000352"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "Virtualization Technology Support",
				"ItemCount": 0,
				"NValue": "600031497",
				"ElementValue": "600031497"
			},
			"NavigationItemList": [
				{
					"Description": "Yes",
					"NValue": "100007671 50001157 4026 600031498",
					"ElementValue": "600031498"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "Thermal Design Power",
				"ItemCount": 0,
				"NValue": "600039173",
				"ElementValue": "600039173"
			},
			"NavigationItemList": [
				{
					"Description": "55W",
					"NValue": "100007671 50001157 4026 600039185",
					"ElementValue": "600039185"
				},
				{
					"Description": "65W",
					"NValue": "100007671 50001157 4026 600039174",
					"ElementValue": "600039174"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "Cooling Device",
				"ItemCount": 0,
				"NValue": "600000360",
				"ElementValue": "600000360"
			},
			"NavigationItemList": [
				{
					"Description": "Heatsink and Fan included",
					"NValue": "100007671 50001157 4026 600000361",
					"ElementValue": "600000361"
				}
			]
		},
		{
			"TitleItem": {
				"Description": "Integrated Graphics",
				"ItemCount": 0,
				"NValue": "600001656",
				"ElementValue": "600001656"
			},
			"NavigationItemList": [
				{
					"Description": "Intel HD Graphics",
					"NValue": "100007671 50001157 4026 600265638",
					"ElementValue": "600265638"
				}
			]
		}
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

## Power Search