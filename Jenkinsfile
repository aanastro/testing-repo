pipeline {
    agent any
    tools {
      maven 'maven 3.8.4'
    }
    stages {
        stage('Compile') {
            steps {
                sh 'mvn clean package -DskipTests=true'
            }
        }
        stage('Unit Tests') {
            steps {
                sh 'mvn surefire:test'
            }
        }
         stage('Integration Tests') {
            steps {
                sh 'mvn failsafe:integration-test'
            }
        }
    }
}
