pipeline {
    agent any
    tools {
        maven 'maven-3.8.8'
    }
    stages {
        stage ('SPRING-PETCLINIC CLONE-STAGE') {
            steps {
            sh 'git clone https://github.com/devopswithcloud/spring-petclinic.git'
            }    
        }
        stage ('MAVEN BUILD') {
            steps {
            sh 'cd /var/lib/jenkins/workspace/WEBHOOK/spring-petclinic'
            sh ' ls -ltr'               
            }
        }
    }
}
