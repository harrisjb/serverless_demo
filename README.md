### What you'll need

1. Amazon developer account
2. AWS Keys for a user with (FYI if you have an admin user it will work):

```
   IAM Full Access
   Api Gateway Admin
   Lambda Full Access
```


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


3. AWS CLI tool if you don't have it 

```brew install awscli```

Configure using `aws configure` and give it your keys, use `us-east-1`
for region and `json` for default format

### Slides

### Getting Started

1. Make sure you have an [AWS account](https://aws.amazon.com) set up `https://aws.amazon.com`

2. Make sure you have an [AWS developer](https://developer.amazon.com/) account set up `https://developer.amazon.com/`

3. Each directory is a different serverless framework or project, cd
   into the directories for instructions in the README files
