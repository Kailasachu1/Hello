pipeline {
    agent any
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
