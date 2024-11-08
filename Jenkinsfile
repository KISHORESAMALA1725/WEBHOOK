pipeline {
    agent {
        label 'java-slave' //
    }
    stages {
        stage ('DEPLOYING NGINX APPLICATION') {
            steps {
                sh 'sudo apt update -y'
                sh 'sudo apt install nginx -y'
                sh 'sudo echo "KISHORE SAMALA" > index.html'
                sh 'sudo acp index.html /var/www/html'
            }
        }
    }
}
