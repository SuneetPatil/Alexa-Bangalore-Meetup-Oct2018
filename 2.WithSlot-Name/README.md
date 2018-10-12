# Build an Alexa Bangalore meetup Skill using slots and built-in slot types
<img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/header._TTH_.png" />

- This tutorial will explains how to use slots and built-in slot type using the code we built in Launch Request section and make use of Welcome Intent.

## For Building Interaction Model 

1. **Build the Interaction Model for your skill**
    1. On the left hand navigation panel, select the **JSON Editor** tab under **Interaction Model**. In the textfield provided, replace any existing code with the code provided in the [Interaction Model](./models/en-US.json).  Click **Save Model**.
    2. If you want to change the skill invocation name, select the **Invocation** tab. Enter a **Skill Invocation Name**. This is the name that your users will need to say to start your skill.  In this case, it's preconfigured to be 'Hello World'.
    3. Click "Build Model".
    
## For Developing Lambda function using AWS
- **Open** this Lambda function [source code file](./lambda/custom/index.js), copy the contents of the file, and paste it into the index.js file.




**or**




1. Update HelloWorldIntentHandler to WelcomeIntentHandler and change the intent name to WelcomeIntent
2. Add line of code to read the name from slot and add to messages
    1. nameSlot = handlerInput.requestEnvelope.request.intent.slots.name.value
    2. Welcome Intent = `Hey ${nameSlot}, Glad that your using our skill`
3. Change the messages
    1. Launch Request Intent = 'Welcome to Alexa Bangalore Meetup Skill.! What is your name?'
    2. Help Intent = 'Your in Alexa Bangalore Meetup Skill.! What is your name?';
4. Add Reprompts for Launch and Help Intent
5. Zip the node module + index.js files and upload in Lambda.
