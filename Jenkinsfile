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
                bat "mvn clean -f helloworld"
            }
        }
        stage('build') {
            steps {
                bat "mvn test -f helloworld"
            }
        }
        stage('upload to nexus') {
            steps {
                bat "mvn package -f helloworld"
            }
        }
    }
}
