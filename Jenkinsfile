pipeline {
    agent any


    stages {


        stage('Build') {
            steps {
                sh "./mvnw clean package"
            }

            post {
                  always {
                       junit '**/target/surefire-reports/TEST-*.xml'
                       archiveArtifacts 'target/*.jar'
                  }
                  failure {
                      echo "failure"
                  }
            }
        }

        stage("Run"){
                   steps{
                       echo "Run "
                  }
            }

         stage("Deploy"){
                    steps{
                      echo "Deploy"
                    }
                }

    }
}
