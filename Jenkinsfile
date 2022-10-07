pipeline {
    agent any
    tools {
  maven 'maven'
}
    triggers {
        pollSCM '* * * * *'
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
             stage('test') {
            steps {
                echo 'test'
            }
        }
             stage('deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
}
