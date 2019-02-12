# An alexa skill that uses DynamoDB

This is a simple skill that will store the movies you watch, and suggest you movies depending 
on the genre you say to it.

It uses a template that shows use of DynamoDB with Alexa. This template uses the [Alexa Skills Kit for Node.js](https://github.com/alexa/alexa-skills-kit-sdk-for-nodejs) version 2.0 and is designed to be used with the [Alexa Skills Kit CLI](https://developer.amazon.com/docs/smapi/ask-cli-intro.html).


## Instructions to execute this template 
- Provide DynamoDB execution permission to the Lambda.
- Create a DynamoDB table with name dynamodb-starter and schema, user Id as a Partition Key and movieTitle as a sort key. 

```
{
    AttributeDefinitions: [
        {
            AttributeName: 'userId',
            AttributeType: 'S'
        },
        {
            AttributeName: 'movieTitle',
            AttributeType: 'S'
        }
    ],
    KeySchema: [
        {
            AttributeName: 'userId',
            KeyType: 'HASH'
        },
        {
            AttributeName: 'movieTitle',
            KeyType: 'RANGE'
        }
    ]
}
```
You can also go to <a href="https://skilltemplates.com/" target="_blank">skilltemplates.com</a> to get working templates with tutorials.
