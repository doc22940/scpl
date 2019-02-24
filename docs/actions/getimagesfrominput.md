
## Get Images from Input / getimagesfrominput (internally `is.workflow.actions.detect.images`)



## description
### summary
Gets images from the result of the previous action.

For example, this action can get the album art of a song, or all the images on a web page.


### usage
`getimagesfrominput `

### arguments


### for developers

<details><summary>source json</summary>
<p>
```json
{
	"ActionClass": "WFCoercionAction",
	"ActionKeywords": [
		"find",
		"search",
		"detect",
		"scan",
		"e-mail",
		"emails"
	],
	"Category": "Photos & Video",
	"CoercionItemClass": "WFImageContentItem",
	"Description": {
		"DescriptionSummary": "Gets images from the result of the previous action.\n\nFor example, this action can get the album art of a song, or all the images on a web page."
	},
	"IconName": "Image.png",
	"Input": {
		"Multiple": true,
		"Required": true,
		"Types": [
			"UIImage"
		]
	},
	"Name": "Get Images from Input",
	"Output": {
		"Multiple": true,
		"OutputName": "Images",
		"Types": [
			"WFImageContentItem"
		]
	},
	"ShortName": "Get Images",
	"Subcategory": "Images"
}
```
</p></details>