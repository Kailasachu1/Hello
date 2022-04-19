pipeline {
    agent any
    tools { 
        maven 'maven_3.8.5' 
        jdk 'jdknew' 
    }
   
    stages {
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = ${PATH}"
                    echo "MAVEN_HOME = ${MAVEN_HOME}"
                ''' 
            }
        }
        stage('code checkout') {
            steps {
                checkout scm
            }
        }
        stage('test') {
            steps {
                call mvn test -f helloworld
            }
        }
        stage('upload to nexus') {
            steps {
                bat "mvn package -f helloworld"
            }
        }
    }
}
