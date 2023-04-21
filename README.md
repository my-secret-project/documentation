# Story Teller Web App - My Hobby Project

This is a hobby project, I do on my spare time and my intention is to learn and make something useful for me, my family. If it's really helpful may be open up for more people, in future.

# Considerations:
## Cost
We need to keep the cost to absolute minimum as there is no timeline. Hence Infrastructure as Code and using Serverless Architecture is the key. 
## Maintenance Effort
We need to automate the entire pipeline, So that changes can be made easy and confidently.
## Tech Stack
The main objective is to learn. So every opportunity will be taken to try something new and do it differently. 
## Security
Even though its a hobby project, we should ensure the application is secured and best practises are followed.

# Design
Here is a simplest view of the project so far. We have react native UI interacts with lambda API backend secured using google firebase.
UI static files are built using [Github actions](https://docs.github.com/en/actions) and published to [AWS S3 bucket](https://aws.amazon.com/s3/) and served to the end user using [AWS Content Delivery Network](https://aws.amazon.com/cloudfront/). 
Lambda API's are built and deployed using [SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/what-is-sam.html)  
![Design](https://github.com/madhusudhanan-mohan/documentation/blob/main/openAI.png?raw=true)

# Lambda's
- [OpenAI Lambda](https://github.com/my-secret-project/lambda/tree/main/src/chatgpt-api)
- [Authenticate API](https://github.com/my-secret-project/lambda/tree/main/src/authenticate)
- [Authorise API](https://github.com/my-secret-project/lambda/tree/main/src/authorise)

# Authorizer
- [cloudformation template](https://github.com/my-secret-project/lambda/blob/main/template.yaml#L52)
- [Google auth token verification](https://github.com/my-secret-project/lambda/blob/main/src/authorise/authValidator.ts#L20)
- [Unit test for Auth verification](https://github.com/my-secret-project/lambda/blob/main/test/hello.spec.js#L31)

# React UI
- [Source](https://github.com/my-secret-project/storytellerweb)
- [Demo](http://madhu-learning-aws-storytellerweb.s3-website-ap-southeast-2.amazonaws.com)

# Admin
- [Firebase Admin](https://console.firebase.google.com/project/story-teller-9c304/overview)
- [OpenAI admin](https://platform.openai.com/account/members)

# Others
- [Spring boot demo application with Aurora DB backend-code](https://github.com/my-secret-project/springboot-demo)
- [Spring boot demo application with Aurora DB backend-demo instance](http://ec2-54-146-77-17.compute-1.amazonaws.com:8080/demo/greeting)
- [Aurora DB provisioning using python boto3](https://github.com/my-secret-project/aurora-mysql)

# About the author
<img src="Madhu.jpg" alt="Madhu" style="height: 100px; width:75px;"/> Madhu is a passionate devops engineer by heart and driven by values, which makes him a valuable asset in any team. He loves his running listening to his favourite music. He loves camping and outdoors. He has a smart kid and loves learning to be a great parent.
