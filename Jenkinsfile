/* groovylint-disable-next-line CompileStatic */
pipeline
{
   agent any
    stages {
        stage('Git Clone') {
             steps {
                git credentialsId: 'GIT_HUB_CREDENTIALS', url: 'https://github.com/kyenzo/spring-petclinic-app.git'
             }      
        }

        stage('Docker build') {
            steps {
                    sh '''mvn compile'''
                }
            
        }

        stage('Run tests') {
        }

        stage('Build Image') {
        // sh 'docker version'
        // sh 'docker build -t spring-petclinic-app .'
        // sh 'docker image list'
        // sh 'docker tag spring-petclinic-app kyenzo/spring-petclinic-app:spring-petclinic-app'
        }
        stage('Push Image') {
        }
        stage('Deploy Container') {
            echo 'Tests'
        }
    }
}
