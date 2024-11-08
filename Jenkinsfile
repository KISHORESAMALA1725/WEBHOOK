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
                }
            }
        }
        stage ('MAVEN BUILD') {
            steps {
            sh 'cd /var/lib/jenkins/workspace/WEBHOOK/spring-petclinic/'
            sh 'mvn package'
            sh 'cd /var/lib/jenkins/workspace/WEBHOOK/spring-petclinic/target'
            sh '"java", "-jar" "spring-petclinic-2.6.0-SNAPSHOT.jar"'                
            }
        }
    }
}
