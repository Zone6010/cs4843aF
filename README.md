# cs4843aF
Final Project for Cloud Computing by Zachary Bowman


# AWS Lex
Amazon Lex is a system hosted by amazon using a similar structure to their "Alexa" product line.  It can be used to create simple bots to provide tasks to, 
such as setting timers, buying things quickly, providing quick Q and A, and other simple tasks.  It can access these options via an Intent.  An Intent is essentially a function which wants to return something to a user, or store data for later depending on it's task.  This task can range from handling and just returning data to the user to more complex server data collecting using a lambda function and attachment to a S3 database.

# Intent
Intents are a major part of AWS Lex as it is the only way it understands its user.  These intents can be defined through a multiple step process involving describing Utterances, Slots, Lambda Handers (On Amazon Lambda, which is a seperate program), and a Return result.  For an example, an utterance could be "help" found in a sentence provided by the user, Slots could be what they want help with like "commands" or "capabilities", the Lambda could be searching the database for what commands are available to this user, and the return would be setting the text for Lex to read back to the user.

# Lambda
Amazon Lambda is a seperate program than Lex but can be handled by the "Alias" system available on Lex.  Lex intents may be given an Alias so that the Lambda may recognize what it is looking for to be able to execute.  The importance of a Lambda function is defined by a user, but without one you can not access a database such as an S3 bucket by the bot, which can be essential if you are building a scraqper of some sort and want Lex hooked up to it for ease on the user. Due to differing means, the results can vary drastically.  One user might wish to have a lambda function so that he can verbally ask for an employee in a database with X credentials and Y salary while doing some other work, but another could be something like a machine learning chatbot which takes numerous entries from a user and stores it for algorithm usage later.
