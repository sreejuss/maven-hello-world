pipeline {
    agent any

    stages {
        stage('clean') {
            steps {
                bat 'mvn clean'
            }
        }
         stage('package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}
