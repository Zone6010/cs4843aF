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

# Project Demo
https://utsa.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=4730fe41-8b60-46be-b2a1-ae8b016833dd

# Lambda 

Lambda expressions are important to the program if you want any sort of variable work done.  This includes times, dates, anything not explicitly given by the user.  In my program they are used to handle dates and time, which are used in the SetTimer, OrderFlowers, and AboutLex Intents.  To set something like this up you have to have an alias for your intent which can been seen by the lambda functions, and when called upon the intent will ping and the lambda will be invoked.  This is how it recieves the time/date which is handled by the server I am currently in, that being N. America East (Virginia).

# Data

In this particular system I did not invoke a data storage such as an S3 bucket; however, there are many benefits to doing so.  Having a storage facility that it can call and read at any time means it would be able to be processed using Machine Learning.  The only "Learning" the system had was voice recognition which was handled by AWS instead of me.  This means there is a lot of room for adaptability in the future for doing things like visual recognition, and sound recognition (i.e. finding out who is talking).
