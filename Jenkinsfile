pipeline {
    agent {
        label 'java-slave'
    }
    tools {
        maven 'maven-3.8.8'
        jdk 'JDK-17'
    }
    stages {
        stage ('SPRING-PETCLINIC CLONE-STAGE') {
            steps {
            sh 'whoami'    
            sh 'git clone https://github.com/devopswithcloud/spring-petclinic.git'
            // sh 'cd /var/lib/jenkins/workspace/WEBHOOK/spring-petclinic/'
            sh 'mvn -f /home/siva/jenkins/workspace/WEBHOOK/spring-petclinic/ package'
            sh 'java -jar /home/siva/jenkins/workspace/WEBHOOK/spring-petclinic/target/spring-petclinic-2.6.0-SNAPSHOT.jar'

            }    
        }
    }
}
