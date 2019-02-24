
## Speak Text / speaktext (internally `is.workflow.actions.speaktext`)

> This action is not yet complete. Some arguments may be missing.



## description
### summary
Speaks the inputted text aloud.


### usage
`speaktext waituntilfinished=[string boolean|variable] undefined=[???] pitch=[string number] undefined=[???] undefined=[???]`

### arguments
### Switch: Wait Until Finished / waituntilfinished (internally `WFSpeakTextWait`)
**Default Value**: true
**Allows Variables**: true


Accepts a string with either true or false
or a variable.

---

This paramtype is not implemented. WFSpeakTextRateParameter

---

### Slider Number: Pitch / pitch (internally `WFSpeakTextPitch`)
**Default Value**: 1
**Allows Variables**: true


Accepts a string 
or variable
containing a number value from 0 to 1.

---

This paramtype is not implemented. WFSpeakTextLanguagePickerParameter

---

This paramtype is not implemented. WFSpeakTextVoicePickerParameter

### for developers

<details><summary>source json</summary>
<p>
```json
{
	"ActionClass": "WFSpeakTextAction",
	"ActionKeywords": [
		"speak",
		"dictate",
		"text",
		"say"
	],
	"Category": "Text",
	"CreationDate": "2014-01-20T06:00:00.000Z",
	"Description": {
		"DescriptionSummary": "Speaks the inputted text aloud."
	},
	"IconName": "Sound.png",
	"Input": {
		"Multiple": true,
		"Required": true,
		"Types": [
			"NSString"
		]
	},
	"InputPassthrough": true,
	"LastModifiedDate": "2015-01-11T06:00:00.000Z",
	"Name": "Speak Text",
	"Parameters": [
		{
			"Class": "WFSwitchParameter",
			"DefaultValue": true,
			"Key": "WFSpeakTextWait",
			"Label": "Wait Until Finished"
		},
		{
			"Class": "WFSpeakTextRateParameter",
			"Key": "WFSpeakTextRate",
			"Label": "Rate"
		},
		{
			"Class": "WFSliderParameter",
			"DefaultValue": 1,
			"Key": "WFSpeakTextPitch",
			"Label": "Pitch",
			"MaximumValue": 2,
			"MinimumValue": 0.5
		},
		{
			"Class": "WFSpeakTextLanguagePickerParameter",
			"DefaultValue": "Default",
			"Key": "WFSpeakTextLanguage",
			"Label": "Language"
		},
		{
			"AlwaysShowsButton": true,
			"Class": "WFSpeakTextVoicePickerParameter",
			"DefaultValue": "Default",
			"DisallowedVariableTypes": [
				"Variable"
			],
			"Key": "WFSpeakTextVoice",
			"Label": "Voice",
			"RequiredResources": [
				{
					"WFParameterKey": "WFSpeakTextLanguage",
					"WFParameterRelation": "??",
					"WFResourceClass": "WFParameterRelationResource"
				}
			],
			"WFSpeakTextLanguageKey": "WFSpeakTextLanguage"
		}
	]
}
```
</p></details>