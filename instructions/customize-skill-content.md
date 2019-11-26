# Build An Alexa High Low Game Skill
<img src="https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/quiz-game/header._TTH_.png" />

Build an engaging high-low game skill. Guess a number, and Alexa will tell you whether the number she has in mind is higher or lower.

## Customize the Skill to be Yours

At this point, you should have a working copy of our Fact skill.  In order to make it your own, you will need to customize it with data and responses that you create.  Here are the things you will need to change:

1.  **New sentences to respond to your users.** There are several sentences and responses that you will want to customize for your skill.

    1. Navigate to the **Code** tab again, and expand the project folder on the left to `Skill Code/lambda`.

    2. Open **[lambda_function.py](../lambda/py/lambda_function.py)**

    3. We are going to be editing a response message when the user exits the skill, so let's only focus on lines `64-71`. This contains all of the code for when a user exits the skill. I am going to be replacing the response message when a user exits the skill from "Thanks for playing!!" to "Thanks for playing, looking forward to playing with you again!". To do this, let's focus on line `67` in particular, and replace the contents:

    Before:
    ```py
    def cancel_and_stop_intent_handler(handler_input):
        """Single handler for Cancel and Stop Intent."""
        # type: (HandlerInput) -> Response
        speech_text = "Thanks for playing!!" # <-- What we want to change

        handler_input.response_builder.speak(
            speech_text).set_should_end_session(True)
        return handler_input.response_builder.response
    ```

    After:
    ```py
    def cancel_and_stop_intent_handler(handler_input):
        """Single handler for Cancel and Stop Intent."""
        # type: (HandlerInput) -> Response
        speech_text = "Thanks for playing, looking forward to playing with you again!" # <-- CHANGED

        handler_input.response_builder.speak(
            speech_text).set_should_end_session(True)
        return handler_input.response_builder.response
    ```

     After you're done editing all of the files necessary, as before, make sure to press **Save**, **Deploy**, and navigate back to the **Testing** tab. When you launch the skill then exit, Alexa should respond with "Thanks for playing, looking forward to playing with you again" instead of "Thanks for playing!!".

2.  **New language.** If you are creating this skill for another language other than English, you will need to make sure Alexa's responses are also in that language.

    - For example, if you are creating your skill in German, every single response that Alexa makes has to be in German. You can't use English responses or your skill will fail certification.

3. **Once you have customized the skill's data, languages and/or sentences, return to the [Amazon Developer Portal](https://developer.amazon.com/alexa/console/ask?&sc_category=Owned&sc_channel=RD&sc_campaign=Evangelism2018&sc_publisher=github&sc_content=Survey&sc_detail=fact-nodejs-V2_GUI-5&sc_funnel=Convert&sc_country=WW&sc_medium=Owned_RD_Evangelism2018_github_Survey_fact-nodejs-V2_GUI-5_Convert_WW_beginnersdevs&sc_segment=beginnersdevs) and select your skill from the list.**

4.  **Click on "Distribution" in the top navigation to move on to the publishing and certification of your skill.**


[![Next](https://m.media-amazon.com/images/G/01/mobile-apps/dex/alexa/alexa-skills-kit/tutorials/general/buttons/button_next_publication._TTH_.png)](./submit-for-certification.md)

