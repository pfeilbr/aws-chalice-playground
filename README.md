# aws-chalice-playground

learn [aws/chalice](https://github.com/aws/chalice)

> framework for writing serverless apps in python. It allows you to quickly create and deploy applications that use AWS Lambda.

## Notes

* focus is on building REST APIs (API Gateway + lambda)
* event sources support - cron, EventBridge, S3, SNS, SQS, Kinesis, DynamoDB
* compiles down to SAM template + zip containing python code + dependencies
* can combine with CDK to get all CDK features + chalice easy workflow/deploy benefits

---

## Demo

```sh
# install in isolated venv via pipx
pipx install chalice

# create new project
chalice new-project helloworld

# deploy
cd helloworld
chalice deploy

# see `helloworld/.chalice` for package artifacts

# test api gateway endpoint
curl https://zqzmirc025.execute-api.us-east-1.amazonaws.com/api/
# output: {"hello":"world"}

# generate package
chalice package packaged/

# SAM template created at `helloworld/packaged/sam.json`
# bundled python code + deps at `helloworld/packaged/deployment.zip`


```

contents of `helloworld/packaged/deployment.zip`

<img src="https://www.evernote.com/l/AAHyCwsWwYtG96AmUf3xm04ZnMMIPOVDlD4B/image.png" alt="" width="75%" />


## Resources

[aws/chalice](https://github.com/aws/chalice)