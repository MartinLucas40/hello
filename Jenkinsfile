pipeline
{
agent any
stages {
    stage('Build') {
        steps {
              sh 'mvn compile'
              }
      }
     stage('Test') {    
        steps {
            sh 'mvn test'
               }
      }
    stage('Package') {
        steps {
            sh 'mvn package -DskipTests'
            }
      }
    stage('Archival') {
        steps {
            archiveArtifacts(onlyIfSuccessful: true, artifacts: '*/*.jar')
              }
      }
    }//stages
environment {
Maven = 'Maven3.6.3'
}
}//pipeline
