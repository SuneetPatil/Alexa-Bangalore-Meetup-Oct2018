# Build a Bangalore Meetup Alexa Skill for Welcoming Audience using only Launch Request
<img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/header._TTH_.png" />

## For Building Interaction Model
1.  **Go to the [Amazon Alexa Developer Portal](http://developer.amazon.com/alexa?&sc_category=Owned&sc_channel=RD&sc_campaign=Evangelism2018&sc_publisher=github&sc_content=Survey&sc_detail=hello-world-nodejs-V2_GUI-1&sc_funnel=Convert&sc_country=WW&sc_medium=Owned_RD_Evangelism2018_github_Survey_hello-world-nodejs-V2_GUI-1_Convert_WW_beginnersdevs&sc_segment=beginnersdevs).  In the top-right corner of the screen, click the "Sign In" button.**

2.  Once you have signed in, move your mouse over the **Developer Console** text at the top of the screen and Select the **Skills** Link.

3.  From the **Alexa Skills Console** select the **Create Skill** button near the top-right of the list of your Alexa Skills.

4. Give your new skill a **Name**. This is the name that will be shown in the Alexa Skills Store, and the name your users will refer to.  For the sake of simplicity, we'll just use **English (US)**.  (You can add other languages later.)  Push Next.

5. Select the **Custom** model button to add it to your skill, and select the **Create Skill** button at the top right.

6. **Build the Interaction Model for your skill**
	1. On the left hand navigation panel, select the **JSON Editor** tab under **Interaction Model**. In the textfield provided, replace any existing code with the code provided in the [Interaction Model](./models/en-US.json).  Click **Save Model**.
    2. If you want to change the skill invocation name, select the **Invocation** tab. Enter a **Skill Invocation Name**. This is the name that your users will need to say to start your skill.  In this case, it's preconfigured to be 'Hello World'.
    3. Click "Build Model".

## For Developing Lambda
1. Git link to download the sample hello world Skill
	https://github.com/alexa/skill-sample-nodejs-hello-world
	
2. Copy and paste only the lambda folder into separate folder and modify your changes.
3. Install the packages using 'npm install' by navigating too lambda\custom
4. Change the messages
	a. Launch Request Intent = 'Welcome to Alexa Bangalore Meetup Skill.!'
	b. Help Intent = 'Your in Alexa Bangalore Meetup Skill.!';
	c. Cancel/Stop Intent = 'Thanks for using Alexa Bangalore Meetup Skill.! Goodbye!'
