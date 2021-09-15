pipeline {
    agent any

    stages {
        stage('clean') {
            steps {
                sh 'mvn clean'
            }
        }
      

         stage('package') {
            steps {
                sh 'mvn install'
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
    }
}
