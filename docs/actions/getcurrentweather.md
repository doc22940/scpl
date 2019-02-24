
## Get Current Weather / getcurrentweather (internally `is.workflow.actions.weather.currentconditions`)

> This action is not yet complete. Some arguments may be missing.


> This action requires that Shortcuts has permission to use WFWeatherAttributionAccessResource,WFLocationAccessResource.


## description
### summary
Gets the current weather conditions at the specified location.


### usage
`getcurrentweather at=[string <${strInfo}>|variable] undefined=[???]`

### arguments
### Enumeration: At / at (internally `WFWeatherLocation`)
**Default Value**: Current Location


Accepts a string 
containing one of the options:

- `Current Location`
- `Custom Location`

---

This paramtype is not implemented. WFLocationFieldParameter

### for developers

<details><summary>source json</summary>
<p>
```json
{
	"ActionClass": "WFGetCurrentWeatherConditionsAction",
	"ActionKeywords": [
		"current",
		"temperature",
		"visibility",
		"humidity",
		"pressure",
		"wind",
		"sunrise",
		"sunset"
	],
	"AppIdentifier": "com.apple.weather",
	"Category": "Location",
	"Description": {
		"DescriptionAttribution": {
			"Description": "Weather information provided by ${Link}",
			"Link": {
				"Text": "The Weather Channel",
				"URL": "https://www.weather.com"
			}
		},
		"DescriptionSummary": "Gets the current weather conditions at the specified location."
	},
	"IconName": "Weather.png",
	"InputPassthrough": false,
	"Name": "Get Current Weather",
	"Output": {
		"Multiple": false,
		"OutputName": "Weather Conditions",
		"Types": [
			"WFWeatherData"
		]
	},
	"Parameters": [
		{
			"Class": "WFEnumerationParameter",
			"DefaultValue": "Current Location",
			"DisallowedVariableTypes": [
				"Ask",
				"Variable"
			],
			"Items": [
				"Current Location",
				"Custom Location"
			],
			"Key": "WFWeatherLocation",
			"Label": "At"
		},
		{
			"Class": "WFLocationFieldParameter",
			"HintDisplayMode": "Never",
			"Key": "WFWeatherCustomLocation",
			"Label": "Location",
			"Placeholder": "Cupertino, CA",
			"RequiredResources": [
				{
					"WFParameterKey": "WFWeatherLocation",
					"WFParameterValue": "Custom Location",
					"WFResourceClass": "WFParameterRelationResource"
				}
			],
			"TextAlignment": "Right"
		}
	],
	"RequiredResources": [
		"WFWeatherAttributionAccessResource",
		"WFLocationAccessResource"
	],
	"Subcategory": "Weather",
	"UnsupportedEnvironments": [
		"Background"
	]
}
```
</p></details>