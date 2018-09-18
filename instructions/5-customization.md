# Build An Alexa High Low Game Skill using ASK Python SDK
<img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/header._TTH_.png" />

[![Voice User Interface](https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/navigation/1-locked._TTH_.png)](./1-voice-user-interface.md)[![Lambda Function](https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/navigation/2-locked._TTH_.png)](./2-lambda-function.md)[![Connect VUI to Code](https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/navigation/3-locked._TTH_.png)](./3-connect-vui-to-code.md)[![Testing](https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/navigation/4-locked._TTH_.png)](./4-testing.md)[![Next Steps](https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/navigation/5-on._TTH_.png)](./5-customization.md)[![Publication](https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/navigation/6-off._TTH_.png)](./6-publication.md)

## Customization / Next Steps

At this point, you should have a working copy of our High Low skill.  In order to make it your own, you will need to customize it with some responses that you create.  Here are the things you will need to change:

1.  **Update your sample utterances.** There are some sample utterances for NumberGuessIntent.  You need to update this list of utterances to for a robust voice experience. **Remember that if you are creating this skill for another language other than English, your sample utterances need to be written in that language, not English.**

  1. **Click the "Save" button when you have completed.**

3.  **New sentences to respond to your users.** There are several sentences and responses that you will want to customize for your skill.

    1.  **Go back to your copy of [lambda_function.py](../lambda/py/lambda_function.py).**

    2.  **Look for lines like this: speech_text = ("Welcome to the High Low guessing game. You have played {} times. "."** These are strings that hold phrases for Alexa to respond with.  Customize them to make it as varied and conversational as time allows.

    3.  **Continue through lambda_function.py until you reach the bottom of the file.**  This will ensure that you cover each of the Alexa responses that you need to update.

4.  **New language.** If you are creating this skill for another language other than English, you will need to make sure Alexa's responses are also in that language.

    *  For example, if you are creating your skill in German, every single response that Alexa makes has to be in German.  You can't use English responses or your skill will fail certification.

5.  **When you have replaced the data in `lambda_function.py`, you need to upload the latest data into Lambda.**  Copy the updated contents into the ``skill_env`` folder, zip the contents of the ``skill_env`` folder and upload it to AWS Lambda as discussed in the "**Finish configuring your function**" step in [Lambda setup documentation](./2-lambda-function.md). Test your skill through the Alexa Simulator on the developer portal, with the updated changes.    

6.  **Once you have made the updates listed on this page, you can click "Launch" in the top navigation to move on to Publishing and Certification of your skill.**

<br/><br/>
<a href="./6-publication.md"><img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/buttons/button_next_publication._TTH_.png" /></a>
