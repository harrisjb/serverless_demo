### What you'll need

1. Amazon developer account
2. AWS Keys for your user

### Slides and docs

### Getting Started

1. Install serverless

`npm install -g serverless`

2. Create project

`serverless create -t aws-nodejs`

3. Add an event endpoint in `serverless.yml`

```
functions:
  hello:
    handler: handler.hello

#    The following are a few example events you can configure
#    NOTE: Please make sure to change your handler code to work with those events
#    Check the event documentation for details
    events:
      - http:
          path: users/create
          method: get

```
