# Build An Alexa Bangalore meetup Skill using custom slot types & Deligate dialogs 
<img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/header._TTH_.png" />

## For Building Interaction Model
- This tutorial will explains how to use custom slot types, Deligate dialogs to fill all the slots and provide user customized messages based on the users input using the code we built in WithSlot-Name section.

1. **Build the Interaction Model for your skill**
    1. On the left hand navigation panel, select the **JSON Editor** tab under **Interaction Model**. In the textfield provided, replace any existing code with the code provided in the [Interaction Model](./models/en-US.json).  Click **Save Model**.
    2. If you want to change the skill invocation name, select the **Invocation** tab. Enter a **Skill Invocation Name**. This is the name that your users will need to say to start your skill.  In this case, it's preconfigured to be 'Hello World'.
    3. Click "Build Model".
    
## For Developing Lambda function using AWS
- **Open** this Lambda function [source code file](./lambda/custom/index.js), copy the contents of the file, and paste it into the index.js file.




**or**




1. Add a code to read background
	a. backgroundSlot = handlerInput.requestEnvelope.request.intent.slots.background.value
2. Add a logic to validate if slots filled
	```
	if (!nameSlot || !backgroundSlot) {
	    return handlerInput.responseBuilder
		.addDelegateDirective()
		.getResponse();
	}
	```
3. Append Customised message based on background and send the message
4. Zip the node module + index.js files and upload in Lambda.
