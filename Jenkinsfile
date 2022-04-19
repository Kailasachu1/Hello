pipeline {
    agent any
        stage('git repo & clean') {
            steps {
                bat "mvn clean -f helloworld"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f helloworld"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f helloworld"
            }
        }
    }
}
