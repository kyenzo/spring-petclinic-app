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
                    sh 'mvn compile -X > debug.log'
            }
        }

        // stage('Run tests') {
        //     steps {
        //         echo 'Hello World'
        //     }
        // }

        // stage('Build Image') {
        //     // sh 'docker version'
        //     // sh 'docker build -t spring-petclinic-app .'
        //     // sh 'docker image list'
        //     // sh 'docker tag spring-petclinic-app kyenzo/spring-petclinic-app:spring-petclinic-app'
        //     steps {
        //         echo 'Hello World'
        //     }
        // }
        // stage('Push Image') {
        //     steps {
        //         echo 'Hello World'
        //     }
        // }
        // stage('Deploy Container') {
        //     steps {
        //         echo 'Hello World'
        //     }
        // }
    }
}
