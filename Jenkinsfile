pipeline {
    agent any
    tools {
        maven 'maven-3.8.8'
    }
    stages {
        stage ('SPRING-PETCLINIC CLONE-STAGE') {
            steps {
            sh 'whoami'    
            sh 'git clone https://github.com/devopswithcloud/spring-petclinic.git'
            sh 'whoami'
            }    
        }
        stage ('MAVEN BUILD') {
            steps {
            sh 'whoami'
            sh 'cd /var/lib/jenkins/workspace/WEBHOOK/spring-petclinic/'
            sh 'whoami'
            sh 'cd spring-petclinic'
            sh 'pwd'
            sh 'ls -ltr'               
            }
        }
    }
}
