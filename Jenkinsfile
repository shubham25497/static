pipeline{
    agent any
      stages{
          stage('Lint HTML') {
            steps {
                sh 'tidy -q -e index.html'
            }
        }
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-2',credentials:'AWS Credentials') {
                    s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'static-jenkins-pipelines-on-aws')
                }
            }
        }
    }
}
