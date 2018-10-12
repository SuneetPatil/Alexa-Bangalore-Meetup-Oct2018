1. Update HelloWorldIntentHandler to WelcomeIntentHandler and change the intent name to WelcomeIntent
2. Add line of code to read the name from slot and add to messages.
	a. nameSlot = handlerInput.requestEnvelope.request.intent.slots.name.value
	b. Welcome Intent = `Hey ${nameSlot}, Glad that your using our skill`;
4. Change the messages
	a. Launch Request Intent = 'Welcome to Alexa Bangalore Meetup Skill.! What is your name?'
	b. Help Intent = 'Your in Alexa Bangalore Meetup Skill.! What is your name?';
5. Add Reprompts for Launch and Help Intent