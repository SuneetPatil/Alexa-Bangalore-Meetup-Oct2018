1. Add a code to read background
	a. backgroundSlot = handlerInput.requestEnvelope.request.intent.slots.background.value
2. Add a logic to validate if slots filled
	if (!nameSlot || !backgroundSlot) {
		return handlerInput.responseBuilder
			.addDelegateDirective()
			.getResponse();
	}
3. Append Customised message based on background and send the message