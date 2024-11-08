pipeline {
    agent any
    tools {
        maven 'maven-3.8.8'
    }
    stages {
        stage ('MAVEN BUILD STAGE') {
            steps {
            sh 'cd /opt'    
            sh 'git clone https://github.com/devopswithcloud/spring-petclinic.git'
            sh 'pwd'
            }
        }
    }
}
