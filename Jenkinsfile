node {

    stage("Git Clone"){

        git credentialsId: 'GIT_HUB_CREDENTIALS', url: 'https://github.com/kyenzo/spring-petclinic-app.git'
    }
    stage('Gradle Build') {

       sh './gradlew build'

    }

    stage("Docker build"){
        sh 'docker version'
        sh 'docker build -t spring-petclinic-app .'
        sh 'docker image list'
        sh 'docker tag spring-petclinic-app kyenzo/spring-petclinic-app:spring-petclinic-app'
    }


    stage('Deploy spring boot') {
          sshCommand remote: remote, command: "kubectl apply -f k8s-spring-boot-deployment.yml"
        
    }
}