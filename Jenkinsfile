pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('This will execute in JAVA_SLAVE') {
            steps {
                sh 'java -version'
            }
        }
        stage ('This stage will execute in DOCKER_SLAVE') {
            agent {
                label 'docker-slave'
            }
            steps {
                sh 'docker version'
            }
        }
    }
}
