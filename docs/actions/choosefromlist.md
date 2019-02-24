
## Choose from List / choosefromlist (internally `is.workflow.actions.choosefromlist`)


> This action requires that Shortcuts has permission to use WFUserInteractionResource.


## description
### summary
Presents a menu of the items passed as input to the action and outputs the user's selection.


### usage
`choosefromlist prompt=[string|text] selectmultiple=[string boolean|variable] selectallinitially=[string boolean|variable]`

### arguments
### Text Input: Prompt / prompt (internally `WFChooseFromListActionPrompt`)
**Placeholder**: optional
**Allows Variables**: true


Accepts a string 
or text
with the text.

---

### Switch: Select Multiple / selectmultiple (internally `WFChooseFromListActionSelectMultiple`)
**Allows Variables**: true


Accepts a string with either true or false
or a variable.

---

### Switch: Select All Initially / selectallinitially (internally `WFChooseFromListActionSelectAll`)
**Allows Variables**: true


Accepts a string with either true or false
or a variable.

### for developers

<details><summary>source json</summary>
<p>
```json
{
	"ActionClass": "WFChooseFromListAction",
	"ActionKeywords": [
		"choose",
		"select",
		"list",
		"options",
		"menu",
		"multiple"
	],
	"Category": "Scripting",
	"CreationDate": "2014-02-05T06:00:00.000Z",
	"Description": {
		"DescriptionSummary": "Presents a menu of the items passed as input to the action and outputs the user's selection."
	},
	"IconName": "Scripting.png",
	"Input": {
		"Multiple": true,
		"Required": true,
		"TypePassthrough": true,
		"Types": [
			"WFImageContentItem",
			"WFDictionaryContentItem",
			"WFContentItem"
		]
	},
	"LastModifiedDate": "2016-11-29T06:00:00.000Z",
	"Name": "Choose from List",
	"Output": {
		"Multiple": false,
		"OutputName": "Chosen Item",
		"Types": [
			"WFContentItem"
		]
	},
	"Parameters": [
		{
			"Class": "WFTextInputParameter",
			"DefaultValue": "",
			"Description": "The instruction provided when the list is presented.",
			"DisallowedVariableTypes": [
				"Ask"
			],
			"Key": "WFChooseFromListActionPrompt",
			"Label": "Prompt",
			"Placeholder": "optional",
			"TextAlignment": "Right"
		},
		{
			"Class": "WFSwitchParameter",
			"DefaultValue": false,
			"Description": "When enabled, multiple items may be chosen from the list.",
			"Key": "WFChooseFromListActionSelectMultiple",
			"Label": "Select Multiple"
		},
		{
			"Class": "WFSwitchParameter",
			"DefaultValue": false,
			"Description": "When enabled, all of the items in the list will start out selected when Choose from List is presented.",
			"Key": "WFChooseFromListActionSelectAll",
			"Label": "Select All Initially",
			"RequiredResources": [
				{
					"WFParameterKey": "WFChooseFromListActionSelectMultiple",
					"WFParameterValue": true,
					"WFResourceClass": "WFParameterRelationResource"
				}
			]
		}
	],
	"RequiredResources": [
		"WFUserInteractionResource"
	],
	"Subcategory": "Lists",
	"UserInterfaces": [
		"WatchKit",
		"UIKit",
		"UIKitWidget"
	]
}
```
</p></details>