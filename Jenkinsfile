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
                bat 'mvn install'
            }
        }
        
            stage('Sonarqube analysis') {
            steps {
                script {
                    withSonarQubeEnv('sonar'){
                        bat 'mvn sonar:sonar -DskipTests'
                     }
                 }
            }
        }
    }
}
