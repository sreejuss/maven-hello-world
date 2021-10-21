pipeline {
    agent {label 'agent' }
    tools { maven 'maven'}


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
        
        stage('package') {
            steps {
                sh 'mvn package'
                archiveArtifacts artifacts: 'target **/*.jar', followSymlinks: false      
            }
        }    
    }
}
