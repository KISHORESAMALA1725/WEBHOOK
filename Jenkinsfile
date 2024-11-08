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
            sh 'pwd'
            }    
        }
        stage (SLEEP FOR 10mins) {
            steps {
                sleep 600
                echo " **** WAITING FOR clone to happen ****** "
            }
        }
        stage ('MAVEN BUILD') {
            steps {
            sh 'cd /var/lib/jenkins/workspace/WEBHOOK/spring-petclinic/'
            // sh 'cd spring-petclinic/'
            // sh 'ls -ltr'
            sh 'mvn package'            
            }
        }
    }
}
