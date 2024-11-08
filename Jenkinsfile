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
        stage ('SLEEP FOR 5mins') {
            steps {
                sleep 300
                echo " ********* WAITING FOR CLONE TO HAPPEN ***********"
            }
        }
        stage ('MAVEN BUILD') {
            steps {
            sh 'cd /var/lib/jenkins/workspace/WEBHOOK/spring-petclinic'
            sh 'mvn package'
            sh '"java", "-jar" "spring-petclinic-2.6.0-SNAPSHOT.jar"'                
            }
        }
    }
}
