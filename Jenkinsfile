pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('DEPLOYING NGINX APPLICATION') {
            steps {
                sh 'apt update -y'
                sh 'apt install nginx -y'
                sh 'echo "KISHORE SAMALA" > index.html'
                sh 'cp index.html /var/www/html'
            }
        }
    }
}
