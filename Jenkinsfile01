pipeline {
    agent any
    environment{
        name = "Jeeva"
        city = "Bangalore"
    }
    stages {
              stage('Dev') {
            steps {
                echo 'Dev Environment'
                sh 'echo "${name}"'
                sh 'echo "${city}"'
            }
        }
          stage('Test') {
            steps {
                echo 'Test Environment'
                sh 'echo "${name}"'
            }
        }
          stage('Prod') {
              input {
                message "Should we continue?"
                ok "Yes, we should."
           }
            steps {
                echo 'Prod Environment'
                sh 'echo "${name}"'
            }
        }
        stage('commands ') {
            steps {
                sh '''
                       date
                       cal 2023
                       ls
                       pwd
                '''
            }
        }
        stage('Environment Varaibles') {
            steps {
              sh 'echo "${BUILD_ID}"'
            }
        }
        }
}
