pipeline{
    agent any
      stages{
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-2',credentials:'AWS Credentials') {
                    s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'static-jenkins-pipelines-on-aws')
                }
            }
        }
    }
}
