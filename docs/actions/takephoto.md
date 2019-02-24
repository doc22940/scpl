
## Take Photo / takephoto (internally `is.workflow.actions.takephoto`)


> This action requires that Shortcuts has permission to use WFUserInteractionResource,WFCameraAccessResource.


## description
### summary
Uses the camera to take photos.

### output
Photo from the camera.

### usage
`takephoto showcamerapreview=[string boolean|variable] wfphotocount=[string integer] camera=[string <${strInfo}>]`

### arguments
### Switch: Show Camera Preview / showcamerapreview (internally `WFCameraCaptureShowPreview`)
**Default Value**: true
**Allows Variables**: true


Accepts a string with either true or false
or a variable.

---

### Stepper Number: wfphotocount / wfphotocount (internally `WFPhotoCount`)
**Default Value**: 1
**Allows Variables**: true


Accepts a string 
or variable
containing an integer value.

---

### Enumeration: Camera / camera (internally `WFCameraCaptureDevice`)
**Default Value**: Back
**Allows Variables**: true


Accepts a string 
or variable
containing one of the options:

- `Front`
- `Back`

### for developers

<details><summary>source json</summary>
<p>
```json
{
	"ActionClass": "WFTakePhotoAction",
	"ActionKeywords": [
		"camera",
		"take",
		"photo"
	],
	"AppIdentifier": "com.apple.camera",
	"Category": "Photos & Video",
	"Description": {
		"DescriptionResult": "Photo from the camera.",
		"DescriptionSummary": "Uses the camera to take photos."
	},
	"InputPassthrough": false,
	"LastModifiedDate": "2015-08-20T07:00:00.000Z",
	"Name": "Take Photo",
	"Output": {
		"Multiple": true,
		"OutputName": "Photo",
		"Required": true,
		"Types": [
			"UIImage"
		]
	},
	"Parameters": [
		{
			"Class": "WFSwitchParameter",
			"DefaultValue": true,
			"Key": "WFCameraCaptureShowPreview",
			"Label": "Show Camera Preview"
		},
		{
			"Class": "WFStepperParameter",
			"DefaultValue": 1,
			"Key": "WFPhotoCount",
			"RequiredResources": [
				{
					"WFParameterKey": "WFCameraCaptureShowPreview",
					"WFParameterValue": true,
					"WFResourceClass": "WFParameterRelationResource"
				}
			],
			"StepperDescription": "Number of Photos",
			"StepperNoun": "Photo",
			"StepperPluralNoun": "Photos",
			"StepperPrefix": "Take"
		},
		{
			"Class": "WFEnumerationParameter",
			"DefaultValue": "Back",
			"Items": [
				"Front",
				"Back"
			],
			"Key": "WFCameraCaptureDevice",
			"Label": "Camera"
		}
	],
	"RequiredResources": [
		"WFUserInteractionResource",
		"WFCameraAccessResource"
	],
	"Subcategory": "Camera",
	"UnsupportedEnvironments": [
		"Extension"
	],
	"UserInterfaces": [
		"UIKit"
	]
}
```
</p></details>