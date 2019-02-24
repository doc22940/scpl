
## Set Brightness / setbrightness (internally `is.workflow.actions.setbrightness`)


> This action requires that Shortcuts has permission to use WFSiriAccessResource.


## description
### summary
Sets the device brightness.


### usage
`setbrightness brightness=[string number]`

### arguments
### Slider Number: Brightness / brightness (internally `WFBrightness`)
**Default Value**: 0.5
**Allows Variables**: true


Accepts a string 
or variable
containing a number value from 0 to 1.

### for developers

<details><summary>source json</summary>
<p>
```json
{
	"ACECommandClass": "SASettingSetBrightness",
	"ACESettingValueKey": "WFBrightness",
	"ActionClass": "WFSetBrightnessAction",
	"ActionKeywords": [
		"screen",
		"display",
		"backlight"
	],
	"Category": "Scripting",
	"Description": {
		"DescriptionSummary": "Sets the device brightness."
	},
	"IconName": "Brightness.png",
	"InputPassthrough": true,
	"Name": "Set Brightness",
	"Parameters": [
		{
			"Class": "WFSliderParameter",
			"DefaultValue": 0.5,
			"Description": "If you set the brightness using a variable, use a number between 0 and 1 (for example, pass 0.5 for half brightness).",
			"Key": "WFBrightness",
			"Label": "Brightness"
		}
	],
	"RequiredResources": [
		"WFSiriAccessResource"
	],
	"Subcategory": "Device"
}
```
</p></details>