pipeline {
    agent any
        stage('git repo & clean') {
            steps {
                //bat "rmdir  /s /q helloworld"
                bat "git clone https://github.com/SravanVenus/Hello.git"
                bat "mvn clean -f helloworld"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f helloworld"
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
