/* groovylint-disable-next-line CompileStatic */
node
{
    stage('Git Clone') {
        git credentialsId: 'GIT_HUB_CREDENTIALS', url: 'https://github.com/kyenzo/spring-petclinic-app.git'
    }

    stage('Docker build') {
    //     withMaven {
    //         sh 'mvn compile'
    /* groovylint-disable-next-line LineLength */
    // } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
        // withMaven(maven: 'my-maven', options: [junitPublisher(healthScaleFactor: 1.0)]) {
        sh './mvnw package'
        // }
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
