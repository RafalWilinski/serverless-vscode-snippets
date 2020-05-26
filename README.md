## Serverless Framework snippets for VS Code

[![Version](https://vsmarketplacebadge.apphb.com/version/rafwilinski.serverless-vscode-snippets.svg)](https://marketplace.visualstudio.com/items?itemName=rafwilinski.serverless-vscode-snippets)
[![Installs](https://vsmarketplacebadge.apphb.com/installs/rafwilinski.serverless-vscode-snippets.svg)](https://marketplace.visualstudio.com/items?itemName=rafwilinski.serverless-vscode-snippets)
[![Ratings](https://vsmarketplacebadge.apphb.com/rating/rafwilinski.serverless-vscode-snippets.svg)](https://marketplace.visualstudio.com/items?itemName=rafwilinski.serverless-vscode-snippets)

This extension contains code snippets for YAML syntax for Vs Code editor.

![Demo](images/demo.gif "Demo")

## Installation

In order to install an extension you need to launch the Command Pallete (Ctrl + Shift + P or Cmd + Shift + P) and type Extensions.
There you have either the option to show the already installed snippets or install new ones. Search for *Serverless Framework Snippets* and install it.

## Snippets

Below is a list of all available snippets and the triggers of each one. To use them simply press `Shift + ^` key and type trigger word.

`|` indicates a list of possible choices.

`slscore` - Serverless Framework project core
```yaml
service: my-sls-project

provider:
  name: aws|azure|google|webtasks|spotinst|kubeless
  runtime: nodejs6.10|python2.6|python3.6|java|swift|php
  memory: 128|256|512|1024

functions:
  
```

`slsfun` - Serverless Framework project core
```yaml
handler:
  handler: handler.handle
  name: handler
  description: Example function
  memorySize: 128|256|512|1024
  runtime: nodejs6.10|python2.6|python3.6|java|swift|php
  timeout: 10
  environment:
    - FOO: BAR
  events:
    
```

`iam` - IAM Role Statements
```yaml
iamRoleStatements:
  - Effect: 'Allow'
    Action:
      - 
    Resource:
      
```
    
`fnjoin` - CloudFormation's Fn::Join function
```yaml
Fn::Join:
  - ''
  - - ''
    - 
```

`vpc` - VPC Setup
```yaml
vpc:
  securityGroupIds:
    - 
  subnetIds:
    - 
```

`pkg` - Project packaging setup
```yaml
package:
  include:
    - .git/**
  exclude:
    - .git/**
  excludeDevDependencies: true
```

`ehttp` - HTTP Event Trigger
```yaml
- http:
    path: users/create
    method: get|post
    cors: true|false
    private: true|false
```

`es3` - S3 Event Trigger
```yaml
- s3:
    bucket: photos
    event: s3:ObjectCreated:*
    rules:
      - prefix: uploads/
      - suffix: .jpg
```

`cron` - Scheduled CloudWatch Expresion
```yaml
- schedule:
    rate: rate(10 seconds|minutes|hours|days)
    enabled: true|false
    input:
      : 
```

[MIT License](https://opensource.org/licenses/MIT) © [Dynobase](https://dynobase.dev)
