# Project Specifics - AWS LEX


# Diagram
Screenshot (210).png in the main folder details how the AWS Lex system works. 

# Intents

Intents that are available on the LEX System provided:

    SetTimer
        -An intent created in order to set an alarm when hooked up to something that can alarm the user, this function can later be modified using lambda expression to hook it up to send an E-Mail to the user. 
    HelpMenu
        -An intent created to aid the user by providing what the system can do, upon recognizing the user wants "help" it will return to the user the commands in the system they can call.
    Repeat
        -An intent to repeat the last phrase given by LEX.  This can be useful to those who can not read the screen for any purpose.
    AboutLex
        -An intent to describe the LEX system's purpose.  It will display the projects' last edited and first edited dates.
    HeyLex
        -An intent to notify LEX that you want it's attention.
    SayHello
        -An intent to greet LEX, it is essentially the "Hello World".
    Cancel
        -An intent to cancel whatever intent is currently active.  
    OrderFlowers
        -An intent to simulate ordering flowers.  It is not hooked up to any stores currently, so it will not purchase anything in reality.
    FallbackIntent
        -An intent to fall back on if nothing else fits the description of the question.  Similar to a "default" in a switch statement for coding.
