
## Get File / getfile (internally `is.workflow.actions.documentpicker.open`)

> This action is not yet complete. Some arguments may be missing.


> This action requires that Shortcuts has permission to use [object Object].


## description
### summary
Get files from iCloud Drive or Dropbox. Turn off “Show Document Picker” to specify a path to retrieve.


### usage
`getfile undefined=[???] showdocumentpicker=[string boolean|variable] selectmultiple=[string boolean|variable] filepath=[string|text] initialpath=[string|text] errorifnotfound=[string boolean|variable]`

### arguments
This paramtype is not implemented. WFStorageServicePickerParameter

---

### Switch: Show Document Picker / showdocumentpicker (internally `WFShowFilePicker`)
**Default Value**: true
**Allows Variables**: true


Accepts a string with either true or false
or a variable.

---

### Switch: Select Multiple / selectmultiple (internally `SelectMultiple`)
**Allows Variables**: true


Accepts a string with either true or false
or a variable.

---

### Text Input: File Path / filepath (internally `WFGetFilePath`)
**Placeholder**: example.txt
**Allows Variables**: true


Accepts a string 
or text
with the text.

---

### Text Input: Initial Path / initialpath (internally `WFGetFileInitialDirectoryPath`)
**Placeholder**: optional
**Allows Variables**: true


Accepts a string 
or text
with the text.

---

### Switch: Error If Not Found / errorifnotfound (internally `WFFileErrorIfNotFound`)
**Default Value**: true
**Allows Variables**: true


Accepts a string with either true or false
or a variable.

### for developers

<details><summary>source json</summary>
<p>
```json
{
	"ActionClass": "WFGetFileAction",
	"ActionKeywords": [
		"pick",
		"select",
		"file",
		"document",
		"filepicker.io",
		"filepicker",
		"ink"
	],
	"Category": "Documents",
	"Description": {
		"DescriptionNote": "In the iCloud picker, tap “Locations” to see document pickers from other apps.",
		"DescriptionSummary": "Get files from iCloud Drive or Dropbox. Turn off “Show Document Picker” to specify a path to retrieve."
	},
	"IconName": "Documents.png",
	"LastModifiedDate": "2017-03-13T05:00:00.000Z",
	"Name": "Get File",
	"Output": {
		"Multiple": true,
		"OutputName": "File",
		"Types": [
			"public.data"
		]
	},
	"Parameters": [
		{
			"AlwaysShowsButton": true,
			"Class": "WFStorageServicePickerParameter",
			"Key": "WFFileStorageService",
			"Label": "Service"
		},
		{
			"Class": "WFSwitchParameter",
			"DefaultValue": true,
			"Key": "WFShowFilePicker",
			"Label": "Show Document Picker"
		},
		{
			"Class": "WFSwitchParameter",
			"DefaultValue": false,
			"Key": "SelectMultiple",
			"Label": "Select Multiple",
			"RequiredResources": [
				{
					"WFParameterKey": "WFShowFilePicker",
					"WFParameterValue": true,
					"WFResourceClass": "WFParameterRelationResource"
				}
			]
		},
		{
			"AutocapitalizationType": "None",
			"Class": "WFTextInputParameter",
			"Description": "The path to retrieve, such as \"/folder/file.txt\"",
			"DisableAutocorrection": true,
			"Key": "WFGetFilePath",
			"KeyboardType": "WebSearch",
			"Label": "File Path",
			"Placeholder": "example.txt",
			"RequiredResources": [
				{
					"WFParameterKey": "WFShowFilePicker",
					"WFParameterValue": false,
					"WFResourceClass": "WFParameterRelationResource"
				}
			],
			"TextAlignment": "Left"
		},
		{
			"AutocapitalizationType": "None",
			"Class": "WFTextInputParameter",
			"DisableAutocorrection": true,
			"Key": "WFGetFileInitialDirectoryPath",
			"KeyboardType": "WebSearch",
			"Label": "Initial Path",
			"Placeholder": "optional",
			"TextAlignment": "Left"
		},
		{
			"Class": "WFSwitchParameter",
			"DefaultValue": true,
			"Key": "WFFileErrorIfNotFound",
			"Label": "Error If Not Found",
			"RequiredResources": [
				{
					"WFParameterKey": "WFShowFilePicker",
					"WFParameterValue": false,
					"WFResourceClass": "WFParameterRelationResource"
				}
			]
		}
	],
	"RequiredResources": [
		{
			"RequiredResources": [
				{
					"WFParameterKey": "WFShowFilePicker",
					"WFParameterValue": true,
					"WFResourceClass": "WFParameterRelationResource"
				}
			],
			"WFResourceClass": "WFUserInteractionResource"
		}
	],
	"Subcategory": "File Storage",
	"UserInterfaces": [
		"UIKit"
	]
}
```
</p></details>