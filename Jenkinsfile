pipeline {
     triggers {
        pollSCM('* * * * *')
}
    agent any
    tools {
  maven 'maven'
}
   
    
    stages {
        stage('code checkout') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'               
            }
        }
             stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        
             stage('deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
}
