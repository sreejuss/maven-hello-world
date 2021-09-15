pipeline {
    agent any

    stages {
        stage('clean') {
            steps {
                bat 'mvn clean'
            }
        }
          stage('Sonarqube analysis') {
            steps {
                script {
                    withSonarQubeEnv('sonar'){
                        sh 'mvn sonar:sonar -DskipTests'
                     }
                 }
            }
        }

         stage('package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}
