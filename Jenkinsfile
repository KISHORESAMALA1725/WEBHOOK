pipeline {
    agent any
    tools {
        maven 'maven-3.8.8'
        JDK 'JDK-17'
    }
    stages {
        stage ('SPRING-PETCLINIC CLONE-STAGE') {
            steps {
            sh 'whoami'    
            sh 'git clone https://github.com/devopswithcloud/spring-petclinic.git'
            sh 'cd /var/lib/jenkins/workspace/WEBHOOK/spring-petclinic/'
            sh 'mvn -f /var/lib/jenkins/workspace/WEBHOOK/spring-petclinic/ package'
            sh '"java", "-jar", "/var/lib/jenkins/workspace/WEBHOOK/spring-petclinic/target/spring-petclinic-2.6.0-SNAPSHOT.jar"'
            }    
        }
        // stage ('SLEEP FOR 10mins') {
        //     steps {
        //         sleep 600
        //         echo " **** WAITING FOR clone to happen ****** "
        //     }
        // }
        // stage ('MAVEN BUILD') {
        //     steps {
        //     sh 'cd /var/lib/jenkins/workspace/WEBHOOK/spring-petclinic/'
        //     // sh 'cd spring-petclinic/'
        //     // sh 'ls -ltr'
        //     sh 'mvn package'            
        //     }
        // }
    }
}
