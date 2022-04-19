pipeline {
    agent any
    stage('code checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('build') {
            steps {
                echo '...Hello-World...'
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
