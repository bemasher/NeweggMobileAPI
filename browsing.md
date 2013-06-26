# Browsing
## Top-Level Menu
The top-level menu which is first presented when clicking Browse contains a list of stores available. To browse sub-categories of each store only the `StoreID` field is required.

### Request
```
GET /Stores.egg/Menus
```

### Response
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
GET /Stores.egg/Categories/1/
```

### Response
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

## Sub-Category Menu
To view sub-categories of a store category browse to: `/Stores.egg/Navigation/{StoreID}/{CategoryID}/{NodeId}/`

### Request
```
GET /Stores.egg/Navigation/1/34/6676/
```

### Response
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