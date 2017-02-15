### What you'll need

1. Amazon developer account
2. AWS Keys for your user

### Getting Started

1. Install serverless

`npm install -g serverless`

2. Create project

`serverless create -t aws-nodejs`

3. Copy `examplehandler.js` to `handler.js` 

```
cp examplehandler.js handler.js
```

4. Add an event alexaSkill in `serverless.yml` for your function

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

12. Upload a picture for your skill (required) and submit
