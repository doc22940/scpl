
## Repeat with Each / repeatwitheach (internally `is.workflow.actions.repeat.each`)



## description
### summary
Takes a list of items as input, and runs the contained actions once for each item in the list.

### input
A list of items

### output
Every item passed to the “End Repeat” action

### usage
`repeatwitheach `

### arguments


### for developers

<details><summary>source json</summary>
<p>
```json
{
	"ActionClass": "WFForEachRepeatAction",
	"ActionKeywords": [
		"loop",
		"while",
		"for"
	],
	"Category": "Scripting",
	"Description": {
		"DescriptionInput": "A list of items",
		"DescriptionResult": "Every item passed to the “End Repeat” action",
		"DescriptionSummary": "Takes a list of items as input, and runs the contained actions once for each item in the list."
	},
	"IconName": "Scripting.png",
	"Input": {
		"Multiple": true,
		"Required": false,
		"Types": [
			"WFContentItem"
		]
	},
	"LastModifiedDate": "2015-05-12T07:00:00.000Z",
	"Name": "Repeat with Each",
	"Output": {
		"Multiple": true,
		"OutputName": "Repeat with Each",
		"Types": [
			"WFContentItem"
		]
	},
	"Subcategory": "Control Flow"
}
```
</p></details>