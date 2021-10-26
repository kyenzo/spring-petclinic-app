pipeline {
    agent any
    tools {
        maven 'mymaven'
        
    }
    stages {
        stage ('Initialize') {
            steps {
                // sh '''
                //     echo "PATH = ${PATH}"
                //     echo "M2_HOME = ${M2_HOME}"
                // '''
                git 'https://github.com/kyenzo/spring-petclinic-app.git'
            }
        }

        stage ('Build') {
            steps {
                // sh 'mvn -Dmaven.test.failure.ignore=true -Dcheckstyle.skip install' 
                sh 'mvn -Dmaven.test.failure.ignore=true install' 
            }
            post {
                success {
                    junit 'target/surefire-reports/*/.xml' 
                }
            }
        }
    }
}