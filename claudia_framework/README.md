### What you'll need

1. Amazon developer account
2. AWS Keys for your user

### Docs

[Claudia Docs](https://claudiajs.com/tutorials/installing.html)
`https://claudiajs.com/tutorials/installing.html`

### Getting Started

Using tutorial at
https://claudiajs.com/tutorials/hello-world-lambda.html

1. Install claudia js

`npm install -g claudia`

2. Create basic function in `hello.js`

```
exports.handler = function (event, context) {
  context.succeed('hello world');
};
```

3. Deploy

```
claudia create --region us-east-1 --handler hello.handler
```
