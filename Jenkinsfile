pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
                script{
                value = sh (
                script: 'jq \'.[0] | .ParameterValue\' setup.json',
                 returnStdout: true
                 ).trim()
                }
            sh "aws cloudformation create-stack --stack-name $value --template-body file://base_cft.yaml --parameters file://setup.json --capabilities CAPABILITY_NAMED_IAM --region us-east-1"
              }
             }
            }
            }
