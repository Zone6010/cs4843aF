# cs4843aF
Final Project for Cloud Computing by Zachary Bowman


# AWS Lex
Amazon Lex is a system hosted by amazon using a similar structure to their "Alexa" product line.  It can be used to create simple bots to provide tasks to, 
such as setting timers, buying things quickly, providing quick Q and A, and other simple tasks.  It can access these options via an Intent.  An Intent is essentially a function which wants to return something to a user, or store data for later depending on it's task.  This task can range from handling and just returning data to the user to more complex server data collecting using a lambda function and attachment to a S3 database.

# Intent
Intents are a major part of AWS Lex as it is the only way it understands its user.  These intents can be defined through a multiple step process involving describing Utterances, Slots, Lambda Handers (On Amazon Lambda, which is a seperate program), and a Return result.  For an example, an utterance could be "help" found in a sentence provided by the user, Slots could be what they want help with like "commands" or "capabilities", the Lambda could be searching the database for what commands are available to this user, and the return would be setting the text for Lex to read back to the user.
