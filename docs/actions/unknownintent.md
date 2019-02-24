
## Unknown Intent / unknownintent (internally `is.workflow.actions.sirikit.donation.handle`)




### usage
`unknownintent showwhenrun=[string boolean|variable]`

### arguments
### Switch: Show When Run / showwhenrun (internally `ShowWhenRun`)
**Default Value**: true
**Allows Variables**: true


Accepts a string with either true or false
or a variable.

### for developers

<details><summary>source json</summary>
<p>
```json
{
	"ActionClass": "WFHandleDonatedIntentAction",
	"Discoverable": false,
	"InputPassthrough": true,
	"Name": "Unknown Intent",
	"Parameters": [
		{
			"Class": "WFSwitchParameter",
			"DefaultValue": true,
			"Key": "ShowWhenRun",
			"Label": "Show When Run"
		}
	]
}
```
</p></details>