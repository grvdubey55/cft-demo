pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name $GlueJobName --template-body file://aws-glue.json --parameters ParameterKey=Name,ParameterValue=$GlueJobName --capabilities CAPABILITY_NAMED_IAM --region 'us-east-1'"
              }
             }
            }
            }
