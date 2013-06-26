# Items
All item requests require the `ItemNumber` field found in each item of the `ProductListItems` list found in a search response: `/Products.egg/{ItemNumber}/`

## Product Details
This request returns details of the item.

### Request
```
GET /Products.egg/19-116-901/ProductDetails
```
### Response
```JSON
{
	"uiVolumeDiscountInfo": null,
	"uiExtendedWarrantyContent": {
		"ItemNumber": null,
		"BrandId": 0,
		"SubcategoryId": 0,
		"MessageType": null,
		"MessageTitle": null,
		"MessageDescription": null,
		"GroupInfo": [
			{
				"GroupID": 120,
				"GroupName": "Service Net Replacement Extended Warranty",
				"GroupDescription": "The product will be replaced and shipped directly to you at no charge.",
				"Summary": "&lt;UL type=disc&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;This program provides replacement coverage for PC peripheral products and consumer electronics&lt;?xml:namespace prefix = o ns = \"urn:schemas-microsoft-com:office:office\" /&gt;&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The coverage begins after the manufacturer’s warranty ends&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The product will be replaced one time only in case of malfunction&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Shipping expenses will be reimbursed if the product needs to be returned&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Customer Support is available 24 hours per day, 7 days per week, 365 days per year&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The Contract is fully transferable&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Coverage is provided by Service Net&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;See&nbsp;&lt;A href=\"http://www.newegg.com/HelpInfo/ExtendedWarranty.aspx#Replacement\"&gt;Terms &amp; Conditions &lt;/A&gt;for additional details of this plan&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;&lt;/UL&gt;",
				"ExtendedWarrantyInfoList": [
					{
						"ItemNumber": "SNET-125335",
						"ItemPrice": 29.99,
						"Description": "1 Year Replacement Extended Service Plan",
						"Years": 1,
						"ComboId": -1,
						"PreSelectedMark": "0",
						"TotalDiscountAmount": 0,
						"SpecialPrice": 34.99,
						"InternalType": 0,
						"ExtendedWarrantyType": 0,
						"SpecialType": "SHOW",
						"GroupID": 120,
						"GroupName": "Service Net Replacement Extended Warranty",
						"GroupDescription": "The product will be replaced and shipped directly to you at no charge.",
						"Summary": "&lt;UL type=disc&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;This program provides replacement coverage for PC peripheral products and consumer electronics&lt;?xml:namespace prefix = o ns = \"urn:schemas-microsoft-com:office:office\" /&gt;&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The coverage begins after the manufacturer’s warranty ends&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The product will be replaced one time only in case of malfunction&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Shipping expenses will be reimbursed if the product needs to be returned&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Customer Support is available 24 hours per day, 7 days per week, 365 days per year&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The Contract is fully transferable&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Coverage is provided by Service Net&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;See&nbsp;&lt;A href=\"http://www.newegg.com/HelpInfo/ExtendedWarranty.aspx#Replacement\"&gt;Terms &amp; Conditions &lt;/A&gt;for additional details of this plan&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;&lt;/UL&gt;",
						"FinalPrice": 29.99,
						"OriginalPrice": 34.99
					},
					{
						"ItemNumber": "SNET-125344",
						"ItemPrice": 54.99,
						"Description": "2 Year Replacement Extended Service Plan",
						"Years": 2,
						"ComboId": -1,
						"PreSelectedMark": "0",
						"TotalDiscountAmount": 0,
						"SpecialPrice": 59.99,
						"InternalType": 0,
						"ExtendedWarrantyType": 0,
						"SpecialType": "SHOW",
						"GroupID": 120,
						"GroupName": "Service Net Replacement Extended Warranty",
						"GroupDescription": "The product will be replaced and shipped directly to you at no charge.",
						"Summary": "&lt;UL type=disc&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;This program provides replacement coverage for PC peripheral products and consumer electronics&lt;?xml:namespace prefix = o ns = \"urn:schemas-microsoft-com:office:office\" /&gt;&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The coverage begins after the manufacturer’s warranty ends&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The product will be replaced one time only in case of malfunction&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Shipping expenses will be reimbursed if the product needs to be returned&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Customer Support is available 24 hours per day, 7 days per week, 365 days per year&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The Contract is fully transferable&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Coverage is provided by Service Net&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;See&nbsp;&lt;A href=\"http://www.newegg.com/HelpInfo/ExtendedWarranty.aspx#Replacement\"&gt;Terms &amp; Conditions &lt;/A&gt;for additional details of this plan&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;&lt;/UL&gt;",
						"FinalPrice": 54.99,
						"OriginalPrice": 59.99
					}
				]
			},
			{
				"GroupID": 169,
				"GroupName": "Service Net Replacement with Accidental Damage Service Plan",
				"GroupDescription": "Accidental Damage from Handling coverage begins at the time of purchase. Mechanical failures are covered after the manufacturers' warranty expires (except 1 yr ADH plan where only ADH coverage exists). Shipping charges are covered under the plan",
				"Summary": "&lt;UL type=disc&gt;\n&lt;UL type=disc&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;This program provides replacement coverage for&nbsp;all IT/CE parts, components&nbsp;and/or devices&nbsp;with a purchase price below $500&lt;?xml:namespace prefix = o ns = \"urn:schemas-microsoft-com:office:office\" /&gt;&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Accidental Damage from Handling Coverage begins on the date of purchase&nbsp; &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Mechanical failures are covered for the term remaining after manufacturer’s warranty expires (except 1 yr ADH plan where only ADH coverage exists). &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Prepaid shipping label will be emailed to you within 1 business day of your claim setup&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Shipping charges are covered under the plan and are also provided as a reimbursement uplift on the 1 yr ADH plan where the manufacturer may not cover shipping on basic mechanical failures during the first year of product ownership. &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Customer Support is available 24 hours per day, 7 days per week, 365 days per year &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The Contract is fully transferable &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Coverage is provided by Service Net &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;See &lt;A href=\"http://www.newegg.com/HelpInfo/ExtendedWarranty.aspx#Replacement\"&gt;Terms &amp; Conditions&lt;/A&gt; for additional details of this plan&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;&lt;/UL&gt;&lt;/UL&gt;\n&lt;P style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;&nbsp;&lt;/P&gt;",
				"ExtendedWarrantyInfoList": [
					{
						"ItemNumber": "SNET-186609",
						"ItemPrice": 29.99,
						"Description": "1 Year Replacement with Accidental Damage Service Plan",
						"Years": 1,
						"ComboId": -1,
						"PreSelectedMark": "0",
						"TotalDiscountAmount": 0,
						"SpecialPrice": 34.99,
						"InternalType": 0,
						"ExtendedWarrantyType": 0,
						"SpecialType": "SHOW",
						"GroupID": 169,
						"GroupName": "Service Net Replacement with Accidental Damage Service Plan",
						"GroupDescription": "Accidental Damage from Handling coverage begins at the time of purchase. Mechanical failures are covered after the manufacturers' warranty expires (except 1 yr ADH plan where only ADH coverage exists). Shipping charges are covered under the plan",
						"Summary": "&lt;UL type=disc&gt;\n&lt;UL type=disc&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;This program provides replacement coverage for&nbsp;all IT/CE parts, components&nbsp;and/or devices&nbsp;with a purchase price below $500&lt;?xml:namespace prefix = o ns = \"urn:schemas-microsoft-com:office:office\" /&gt;&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Accidental Damage from Handling Coverage begins on the date of purchase&nbsp; &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Mechanical failures are covered for the term remaining after manufacturer’s warranty expires (except 1 yr ADH plan where only ADH coverage exists). &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Prepaid shipping label will be emailed to you within 1 business day of your claim setup&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Shipping charges are covered under the plan and are also provided as a reimbursement uplift on the 1 yr ADH plan where the manufacturer may not cover shipping on basic mechanical failures during the first year of product ownership. &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Customer Support is available 24 hours per day, 7 days per week, 365 days per year &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The Contract is fully transferable &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Coverage is provided by Service Net &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;See &lt;A href=\"http://www.newegg.com/HelpInfo/ExtendedWarranty.aspx#Replacement\"&gt;Terms &amp; Conditions&lt;/A&gt; for additional details of this plan&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;&lt;/UL&gt;&lt;/UL&gt;\n&lt;P style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;&nbsp;&lt;/P&gt;",
						"FinalPrice": 29.99,
						"OriginalPrice": 34.99
					},
					{
						"ItemNumber": "SNET-186618",
						"ItemPrice": 54.99,
						"Description": "2 Year Replacement with Accidental Damage Service Plan",
						"Years": 2,
						"ComboId": -1,
						"PreSelectedMark": "0",
						"TotalDiscountAmount": 0,
						"SpecialPrice": 59.99,
						"InternalType": 0,
						"ExtendedWarrantyType": 0,
						"SpecialType": "SHOW",
						"GroupID": 169,
						"GroupName": "Service Net Replacement with Accidental Damage Service Plan",
						"GroupDescription": "Accidental Damage from Handling coverage begins at the time of purchase. Mechanical failures are covered after the manufacturers' warranty expires (except 1 yr ADH plan where only ADH coverage exists). Shipping charges are covered under the plan",
						"Summary": "&lt;UL type=disc&gt;\n&lt;UL type=disc&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;This program provides replacement coverage for&nbsp;all IT/CE parts, components&nbsp;and/or devices&nbsp;with a purchase price below $500&lt;?xml:namespace prefix = o ns = \"urn:schemas-microsoft-com:office:office\" /&gt;&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Accidental Damage from Handling Coverage begins on the date of purchase&nbsp; &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Mechanical failures are covered for the term remaining after manufacturer’s warranty expires (except 1 yr ADH plan where only ADH coverage exists). &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Prepaid shipping label will be emailed to you within 1 business day of your claim setup&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Shipping charges are covered under the plan and are also provided as a reimbursement uplift on the 1 yr ADH plan where the manufacturer may not cover shipping on basic mechanical failures during the first year of product ownership. &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Customer Support is available 24 hours per day, 7 days per week, 365 days per year &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;The Contract is fully transferable &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;Coverage is provided by Service Net &lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;\n&lt;LI style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;See &lt;A href=\"http://www.newegg.com/HelpInfo/ExtendedWarranty.aspx#Replacement\"&gt;Terms &amp; Conditions&lt;/A&gt; for additional details of this plan&lt;o:p&gt;&lt;/o:p&gt;&lt;/LI&gt;&lt;/UL&gt;&lt;/UL&gt;\n&lt;P style=\"MARGIN: 0in 0in 0pt; mso-margin-top-alt: auto; mso-margin-bottom-alt: auto; mso-list: l0 level1 lfo1; tab-stops: list .5in\" class=MsoNormal&gt;&nbsp;&lt;/P&gt;",
						"FinalPrice": 54.99,
						"OriginalPrice": 59.99
					}
				]
			}
		]
	},
	"DriveSaverGroupList": null,
	"HasSimilarURL": true,
	"NValue": "similar19-116-901",
	"ItemType": {
		"IsDigitalRiverItem": false,
		"IsDVDItem": false,
		"IsOpenBoxItem": false,
		"IsRecertifiedItem": false,
		"IsAITItem": false,
		"IsPhoneItem": false,
		"IsServicePlanItem": false,
		"IsSimCardItem": false,
		"IsRestrictedItem": false,
		"IsComboBundle": false,
		"IsSimplxityItem": false
	},
	"ReturnPolicyInfo": {
		"Name": "CPU Replacement Only Return Policy",
		"ID": "39",
		"HtmlContent": null,
		"IsSeller": false
	},
	"MailInRebateInfo": null,
	"imageGallery": [
		{
			"ItemNumber": null,
			"Title": null,
			"FullPath": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S640W$",
			"ThumbnailImagePath": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S125W$",
			"SmallImagePath": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S180W$",
			"PathSize35": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S100$",
			"PathSize60": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S125W$",
			"PathSize100": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S180W$",
			"PathSize125": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S180W$",
			"PathSize180": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S300W$",
			"PathSize300": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S640W$",
			"PathSize640": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S640W$"
		}
	],
	"ShippingInfo": {
		"NormalShippingText": "Free Shipping*",
		"SpecialShippingText": " Additional fees may apply for shipments to APO/FPO, AK, HI and PR.",
		"RestrictedShippingTitle": "Shipping Restrictions",
		"RestrictedShippingText": " Additional fees may apply for shipments to APO/FPO, AK, HI and PR."
	},
	"IsShowSoldOutText": false,
	"AddToCartButtonText": "Add to Cart",
	"AddToCartButtonType": "AD",
	"CoremetricsInfo": {
		"CategoryID": "IPS343",
		"ProductName": "CPU INTEL|CORE I7-4770K 3.5G 4C 8M_19-116-901",
		"PageID": "PRODUCT: CPU INTEL|CORE I7-4770K 3.5G 4C 8M_19-116-901 (19-116-901)",
		"Brand": "Intel"
	},
	"EmailFriendImageInfo": {
		"ItemNumber": null,
		"Title": null,
		"FullPath": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S100$",
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
	"ShippingPromotionInfo": null,
	"IsActivated": true,
	"SellerItemPropertyList": null,
	"IsShowEnergyStarSection": false,
	"EnergyStarText": null,
	"IronEggDescription": null,
	"IronEggImageLink": null,
	"ComboCount": 21,
	"SubCategoryId": 343,
	"SubCategoryName": "Processors - Desktops",
	"Warnings": null,
	"IsShipByNewegg": true,
	"ShoppingInsight": {
		"Description": "See what other informed Newegg customers purchased after viewing this product",
		"PromotionItems": [
			{
				"Percentage": "46",
				"IsCurrentItem": true,
				"ItemNumber": "19-116-901",
				"Title": "Intel Core i7-4770K Haswell 3.5GHz LGA 1150 84W Quad-Core Desktop Processor Intel HD Graphics BX80646I74770K",
				"OriginalPrice": "$349.99",
				"IsShowOriginalPrice": false,
				"FinalPrice": "$349.99",
				"ItemImage": {
					"ItemNumber": null,
					"Title": null,
					"FullPath": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S300W$",
					"ThumbnailImagePath": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S125W$",
					"SmallImagePath": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S180W$",
					"PathSize35": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S100$",
					"PathSize60": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S125W$",
					"PathSize100": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S180W$",
					"PathSize125": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S180W$",
					"PathSize180": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S300W$",
					"PathSize300": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S640W$",
					"PathSize640": "http://images17.newegg.com/is/image/newegg/19-116-901-Z01?$S640W$"
				},
				"ItemBrand": null,
				"Instock": true,
				"AfterRebate": null,
				"IsFreeShipping": true,
				"ReviewSummary": {
					"Rating": 0,
					"TotalReviews": "[]"
				},
				"MappingFinalPrice": null,
				"ItemMapPriceMarkType": 0,
				"IsMicrosoftDownloadItem": false,
				"IsProductKeyOnly": false
			},
			{
				"Percentage": "1",
				"IsCurrentItem": false,
				"ItemNumber": "19-116-501",
				"Title": "Intel Core i7-3770K Ivy Bridge 3.5GHz (3.9GHz Turbo) LGA 1155 77W Quad-Core Desktop Processor Intel HD Graphics 4000 BX80637I73770K",
				"OriginalPrice": "$319.99",
				"IsShowOriginalPrice": false,
				"FinalPrice": "$319.99",
				"ItemImage": {
					"ItemNumber": null,
					"Title": null,
					"FullPath": "http://images17.newegg.com/is/image/newegg/19-116-501-Z01?$S300W$",
					"ThumbnailImagePath": "http://images17.newegg.com/is/image/newegg/19-116-501-Z01?$S125W$",
					"SmallImagePath": "http://images17.newegg.com/is/image/newegg/19-116-501-Z01?$S180W$",
					"PathSize35": "http://images17.newegg.com/is/image/newegg/19-116-501-Z01?$S100$",
					"PathSize60": "http://images17.newegg.com/is/image/newegg/19-116-501-Z01?$S125W$",
					"PathSize100": "http://images17.newegg.com/is/image/newegg/19-116-501-Z01?$S180W$",
					"PathSize125": "http://images17.newegg.com/is/image/newegg/19-116-501-Z01?$S180W$",
					"PathSize180": "http://images17.newegg.com/is/image/newegg/19-116-501-Z01?$S300W$",
					"PathSize300": "http://images17.newegg.com/is/image/newegg/19-116-501-Z01?$S640W$",
					"PathSize640": "http://images17.newegg.com/is/image/newegg/19-116-501-Z01?$S640W$"
				},
				"ItemBrand": null,
				"Instock": true,
				"AfterRebate": null,
				"IsFreeShipping": true,
				"ReviewSummary": {
					"Rating": 0,
					"TotalReviews": "[]"
				},
				"MappingFinalPrice": null,
				"ItemMapPriceMarkType": 0,
				"IsMicrosoftDownloadItem": false,
				"IsProductKeyOnly": false
			},
			{
				"Percentage": "1",
				"IsCurrentItem": false,
				"ItemNumber": "19-116-900",
				"Title": "Intel Core i7-4770 Haswell 3.4GHz LGA 1150 84W Quad-Core Desktop Processor Intel HD Graphics BX80646I74770",
				"OriginalPrice": "$319.99",
				"IsShowOriginalPrice": true,
				"FinalPrice": "$309.99",
				"ItemImage": {
					"ItemNumber": null,
					"Title": null,
					"FullPath": "http://images17.newegg.com/is/image/newegg/19-116-900-Z01?$S300W$",
					"ThumbnailImagePath": "http://images17.newegg.com/is/image/newegg/19-116-900-Z01?$S125W$",
					"SmallImagePath": "http://images17.newegg.com/is/image/newegg/19-116-900-Z01?$S180W$",
					"PathSize35": "http://images17.newegg.com/is/image/newegg/19-116-900-Z01?$S100$",
					"PathSize60": "http://images17.newegg.com/is/image/newegg/19-116-900-Z01?$S125W$",
					"PathSize100": "http://images17.newegg.com/is/image/newegg/19-116-900-Z01?$S180W$",
					"PathSize125": "http://images17.newegg.com/is/image/newegg/19-116-900-Z01?$S180W$",
					"PathSize180": "http://images17.newegg.com/is/image/newegg/19-116-900-Z01?$S300W$",
					"PathSize300": "http://images17.newegg.com/is/image/newegg/19-116-900-Z01?$S640W$",
					"PathSize640": "http://images17.newegg.com/is/image/newegg/19-116-900-Z01?$S640W$"
				},
				"ItemBrand": null,
				"Instock": true,
				"AfterRebate": null,
				"IsFreeShipping": true,
				"ReviewSummary": {
					"Rating": 0,
					"TotalReviews": "[]"
				},
				"MappingFinalPrice": null,
				"ItemMapPriceMarkType": 0,
				"IsMicrosoftDownloadItem": false,
				"IsProductKeyOnly": false
			}
		]
	},
	"ProductProperties": null,
	"EduHelpInfo": null,
	"IsCellPhoneItem": false,
	"ShowOriginalPrice": false,
	"MailInRebateText": null,
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
		"TotalReviews": "[39]"
	},
	"Image": {
		"ItemNumber": null,
		"Title": null,
		"FullPath": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S640W$",
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
	"NeweggItemNumber": null,
	"PromotionInfo": null,
	"InstockForCombo": false,
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
	"BrandInfo": {
		"Code": 0,
		"BrandId": 1157,
		"Description": "Intel",
		"ManufactoryWeb": "http://www.intel.com",
		"WebSiteURL": null,
		"HasManfactoryLogo": true,
		"BrandImage": "http://images10.newegg.com/brandimage/Brand1157.gif"
	},
	"LimitQuantity": 5,
	"IsShellShockerItem": false,
	"PromotionText": "Free Skull T-Shirt & $15 gift card w/ purchase, limited offer",
	"ItemMapPriceMarkType": 0,
	"IsHot": false,
	"IsPreLaunch": false,
	"ItemNumber": "19-116-901",
	"Academic": false
}
```

## Product Specifications
A list of product specifications may be obtained using the following request.
### Request
```
GET /Products.egg/19-116-901/Specification/
```

### Response
```JSON
{
	"NeweggItemNumber": "N82E16819116901",
	"Title": "Intel Core i7-4770K Haswell 3.5GHz LGA 1150 84W Quad-Core Desktop Processor Intel HD Graphics BX80646I74770K",
	"SpecificationGroupList": [
		{
			"GroupName": "Model",
			"SpecificationPairList": [
				{
					"Key": "Brand",
					"Value": "Intel"
				},
				{
					"Key": "Series",
					"Value": "Core i7"
				},
				{
					"Key": "Model",
					"Value": "BX80646I74770K"
				}
			]
		},
		{
			"GroupName": "CPU Socket Type",
			"SpecificationPairList": [
				{
					"Key": "CPU Socket Type",
					"Value": "LGA 1150"
				}
			]
		},
		{
			"GroupName": "Tech Spec",
			"SpecificationPairList": [
				{
					"Key": "Core",
					"Value": "Haswell"
				},
				{
					"Key": "Multi-Core",
					"Value": "Quad-Core"
				},
				{
					"Key": "Name",
					"Value": "Core i7-4770K"
				},
				{
					"Key": "Operating Frequency",
					"Value": "3.5GHz"
				},
				{
					"Key": "L3 Cache",
					"Value": "8MB"
				},
				{
					"Key": "Manufacturing Tech",
					"Value": "22 nm"
				},
				{
					"Key": "64 bit Support",
					"Value": "Yes"
				},
				{
					"Key": "Hyper-Threading Support",
					"Value": "Yes"
				},
				{
					"Key": "Integrated Memory Controller Speed",
					"Value": "DDR3"
				},
				{
					"Key": "Virtualization Technology Support",
					"Value": "Yes"
				},
				{
					"Key": "Integrated Graphics",
					"Value": "Intel HD Graphics"
				},
				{
					"Key": "Thermal Design Power",
					"Value": "84W"
				}
			]
		}
	]
}
```

## Combo Deals
### Request
```
GET /Products.egg/19-116-901/ComboDeals/?SubCategory=343&SortField=0&PageNumber=1
```

### Response
```JSON
{
	"PageCount": 26,
	"PageInfo": {
		"TotalCount": 10,
		"PageSize": 10,
		"PageNumber": 1,
		"PageCount": 26,
		"PageNumberList": null
	},
	"ComboList": [
		{
			"ComboItemsCount": 18,
			"ComboType": 0,
			"LimitQuantity": 0,
			"ComboId": 1351996,
			"ComboGroupId": 280446,
			"TotalDiscount": "-$274.83",
			"OriginalPrice": "$3,764.82",
			"IsShowOriginalPrice": true,
			"ComboPrice": "$3,489.99",
			"ComboStockType": 1,
			"IsComboBundle": true,
			"ComboProductList": [
				{
					"GiftDiscount": "$0.00",
					"IsGift": false,
					"MainItemNumber": null,
					"IsCategoryCombo": false,
					"IsCellPhoneItem": false,
					"ShowOriginalPrice": false,
					"MailInRebateText": null,
					"IsComboBundle": false,
					"ProductStockType": 0,
					"MappingFinalPrice": null,
					"IsFeaturedItem": false,
					"IsMicrosoftDownloadItem": false,
					"IsProductKeyOnly": false,
					"Title": "SAMSUNG S23C570H Glossy Black 23\" 5ms (GTG) HDMI Widescreen LED Backlight LCD Monitor",
					"OriginalPrice": "$239.99",
					"Discount": "$20.00",
					"FinalPrice": "$219.99",
					"FreeShippingFlag": false,
					"Model": null,
					"ReviewSummary": null,
					"Image": {
						"ItemNumber": null,
						"Title": null,
						"FullPath": "http://images17.newegg.com/is/image/newegg/24-001-804-TS?$S125W$",
						"ThumbnailImagePath": "http://images17.newegg.com/is/image/newegg/24-001-804-TS?$S125W$",
						"SmallImagePath": "http://images17.newegg.com/is/image/newegg/24-001-804-TS?$S180W$",
						"PathSize35": "http://images17.newegg.com/is/image/newegg/24-001-804-TS?$S100$",
						"PathSize60": "http://images17.newegg.com/is/image/newegg/24-001-804-TS?$S125W$",
						"PathSize100": "http://images17.newegg.com/is/image/newegg/24-001-804-TS?$S180W$",
						"PathSize125": "http://images17.newegg.com/is/image/newegg/24-001-804-TS?$S180W$",
						"PathSize180": "http://images17.newegg.com/is/image/newegg/24-001-804-TS?$S300W$",
						"PathSize300": "http://images17.newegg.com/is/image/newegg/24-001-804-TS?$S640W$",
						"PathSize640": "http://images17.newegg.com/is/image/newegg/24-001-804-TS?$S640W$"
					},
					"SellerName": null,
					"ParentItem": null,
					"SellerId": null,
					"ShipByNewegg": 1,
					"ItemGroupID": 0,
					"ItemOwnerType": 0,
					"NumberOfReviews": 0,
					"AverageRating": 0,
					"Instock": false,
					"XmlSpec": null,
					"WarrantyInfo": null,
					"NeweggItemNumber": null,
					"PromotionInfo": null,
					"InstockForCombo": false,
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
					"PromotionText": null,
					"ItemMapPriceMarkType": 0,
					"IsHot": false,
					"IsPreLaunch": false,
					"ItemNumber": "24-001-804",
					"Academic": false
				},
				...
			],
			"IsContainAndShowComboMIR": false,
			"ComboProductMIR": null,
			"ComboMIR": null,
			"IsShowComboPriceAfterMIR": false,
			"ComboPriceAfterMIRDescription": null,
			"IsShellShockerItem": false,
			"ComboHasMapprice": false,
			"ComboImage": {
				"ItemNumber": null,
				"Title": "6x SAMSUNG 23\" Widescreen LED Monitor, ASUS Radeon HD 7970 3GB, Hex Display Stand, Intel i7 Core Haswell, ASUS SABERTOOTH MOBO, G.SKILL 16GB MEM,  512GB SSD, CORSAIR 850W PSU",
				"FullPath": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll300/combo1351996.jpg",
				"ThumbnailImagePath": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll125/combo1351996.jpg",
				"SmallImagePath": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll200/combo1351996.jpg",
				"PathSize35": "http://images10.newegg.com/ProductImageCompressAll100/combo1351996.jpg",
				"PathSize60": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll125/combo1351996.jpg",
				"PathSize100": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll200/combo1351996.jpg",
				"PathSize125": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll200/combo1351996.jpg",
				"PathSize180": "http://images10.newegg.com/NeweggImage/ProductImageCompressAll300/combo1351996.jpg",
				"PathSize300": "http://images10.newegg.com/NeweggImage/productimage/combo1351996.jpg",
				"PathSize640": "http://images10.newegg.com/NeweggImage/productimage/combo1351996.jpg"
			},
			"RelatedItemNumber": "19-116-901",
			"ComboMapPriceMarkType": 0,
			"MappingFinalPrice": null,
			"EduHelpInfo": null,
			"Academic": false
		},
		...
	]
}
```

## Reviews
### Request
```
GET /Products.egg/19-116-901/Reviewsinfo/1?filter.time=all&filter.rating=All&sort=
```

### Response
```JSON
{
	"IpadReviews": [
		{
			"BoughtTimeTypeInt": 3,
			"TechLevelTypeInt": 4,
			"reviewID": 3802739,
			"Title": "Great CPU, not the best sample",
			"Rating": 4,
			"PublishDate": "6/25/2013 4:31:21 PM",
			"LoginNickName": "XD_40",
			"BoughtTimeTypeString": "1 week to 1 month",
			"TechLevelTypeString": "Somewhat High",
			"IsNewReview": true,
			"PurchaseMark": true,
			"Cons": "I didn't win the chip lottery for overclocking. Got one from Newegg on 6/9/13. It takes 1.275v to hit 4.4 GHz stable. Not impressive for many that are out there. For gaming, 4670K is the better value. But if Crysis 3 sets a trend, the additional threads might help for future games.",
			"Pros": "Fast, low power draw. Blew my old X3380 out of the water in pretty much all benchmarks that I have tracked. Huge jump in minimum FPS in many games. Good bump in quite a few Average FPS.",
			"Comments": "Paired with 2x GTX 680s, 16 GB RAM, Samsung 840 pro SSD. I run it on a custom water cooling setup. During testing for 4.6 GHz, requiring above 1.3v, temperatures did get into mid 90s running SiSoftware Sandra.",
			"TotalConsented": 0,
			"TotalVoting": 0
		},
		...
	],
	"ReviewSummaryInfo": {
		"Last2WeeksCount": 25,
		"Last2WeeksDesc": null,
		"Last6MonthsCount": 39,
		"Last6MonthsDesc": null,
		"AllReviewCount": 39,
		"AllReviewDesc": null
	},
	"Summary": {
		"Rating": 5,
		"TotalReviews": "39"
	},
	"Reviews": null,
	"PaginationInfo": {
		"TotalCount": 39,
		"PageSize": 10,
		"PageNumber": 1,
		"PageCount": 0,
		"PageNumberList": null
	},
	"ProductImageInfo": {
		"Title": null,
		"FullPath": "http://images17.newegg.com/is/image/newegg/19-116-901-TS?$S640W$",
		"ThumbnailImagePath": null,
		"SmallImagePath": null,
		"PathSize35": null,
		"PathSize60": null,
		"PathSize100": null,
		"PathSize125": null,
		"PathSize180": null,
		"PathSize300": null,
		"PathSize640": null
	},
	"ProductReviewBarInfo": {
		"RatingCounts": 39,
		"Rating1Count": "0",
		"Rating1Percent": 0,
		"Rating2Count": "1",
		"Rating2Percent": 3,
		"Rating3Count": "4",
		"Rating3Percent": 10,
		"Rating4Count": "8",
		"Rating4Percent": 21,
		"Rating5Count": "26",
		"Rating5Percent": 67
	}
}
```

### Filtering and Sorting
Filtering and sorting reviews can be done using the following get request values:

#### Rating
<table>
	<tr><th>Value (filter.rating)</th><th>Description</th></tr>
	<tr><td>All</td><td>All Reviews (default)</td></tr>
	<tr><td>5</td><td>5-Egg Reviews</td></tr>
	<tr><td>4</td><td>4-Egg Reviews</td></tr>
	<tr><td>3</td><td>3-Egg Reviews</td></tr>
	<tr><td>2</td><td>2-Egg Reviews</td></tr>
	<tr><td>1</td><td>1-Egg Reviews</td></tr>
</table>

#### Sorting
<table>
	<tr><th>Value (sort)</th><th>Description</th></tr>
	<tr><td>date posted</td><td>Date Posted (default)</td></tr>
	<tr><td>most helpful</td><td>Most Helpful</td></tr>
	<tr><td>highest rated</td><td>Highest Rated</td></tr>
	<tr><td>lowest rated</td><td>Lowest Rated</td></tr>
	<tr><td>ownership</td><td>Ownership</td></tr>
</table>

#### Exceptions
 * `filter.time` never appears to be used in the iPhone application.