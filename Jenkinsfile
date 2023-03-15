pipeline {
    agent any
    stages{
         withAWS(credentials: 'aws_creds', region: 'us-east-1') {
            stage("Submit Stack"){
                steps{
                    sh "aws cloudformation create-stack --stack-name s3bucket --template-body file://simplests3cft.json --region 'us-east-1'"
                }
            }
        }
    }
}
