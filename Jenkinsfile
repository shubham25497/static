pipeline{
    agent any
      stages{
        stages('Build'){
          steps{
            sh  'echo "Hello World"'
            sh '''
              echo "Multiline shell steps works to"
              ls -lah
              '''
          }
        }
    }
}
