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
        stage ('TIMEOUT FOR GIT CLONE') {
            steps {
                timeout (time: 180, unit: 'SECONDS') {
                echo "Waiting for clone to happen"
                sleep 180
                }
            }
        }
        stage ('MAVEN BUILD') {
            steps {
            sh 'mvn package'
            sh '"java", "-jar" "spring-petclinic-2.6.0-SNAPSHOT.jar"'                
            }
        }
    }
}
