pipeline{agent any 
  stages{ stage('Clone Repo') 
          { steps 
                  { sh "export AWS_DEFAULT_REGION=us-east-1"
                    sh "aws cloudformation create-stack --stack-name ${params.stackname} --template-body file://ec2.json --region 'us-east-1' --parameters ParameterKey='InstanceType',ParameterValue=${params.InstanceType} ParameterKey='SSHLocation',ParameterValue=${params.MyIP}" 
           }
         }
      }
	  }
