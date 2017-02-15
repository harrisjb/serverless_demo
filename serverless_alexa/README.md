### What you'll need

1. Amazon developer account
2. AWS Keys for a user with:
  - IAM Full Access
  - Api Gateway Admin
  - Lambda Full Access


As well as the custom permission:
```
{
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "cloudformation:CreateStack",
                "cloudformation:UpdateStack"
            ],
            "Resource": [
                "*"
            ]
        }
    ]
}
```

### Getting Started

1. Install serverless `npm install -g serverless`
2. Create project `serverless create -t aws-nodejs`
3. Copy my `examplehandler.js` into your `handler.js` 
4. Add an event alexaSkill in `serverless.yml` for your function

NOTE: the default function that gets created is hello, you will need to
remove this and replace with the following: 

```
functions:
  catFact:
    handler: handler.catFacts

    events:
      - alexaSkill
```

5. Deploy lambda function

```
serverless deploy
```

6. Login to developer.amazon.com, click on Alexa in nav bar

7. Under Alexa Skills Kit, click Get Started, select Add a New Skill
  - Name your skill last_name_serverless_demo so you know it's yours
(alexa skills do not enforce uniqueness in names right now)

8. Copy intent_schema.json into intent schema field, copy
   sample_utterances.txt into sample utterances field

9. For Interaction Model, select AWS Lambda ARN, and use `serverless
   info` to get ARN from deployed function

10. Test It

11. Configure it as you want, make skill more complex, redeploy

12. Upload a picture for your skill (required), tell them how to test
    it, and submit

This tutorial is based on:
-  https://developer.amazon.com/blogs/post/Tx3DVGG0K0TPUGQ/updated-alexa-skills-kit-fact-template-step-by-step-guide-to-build-a-fact-skill
