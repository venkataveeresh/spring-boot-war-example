pipeline {
  agent any
    environment {
        GIT_REPO = 'https://github.com/venkataveeresh/spring-boot-war-example.git'
        BRANCH = 'master'
        GIT_CRED = 'cda19750-9b34-4f54-b15b-1a26d0eb4949'
    }

    stages {
        stage('Checkout') {
            steps {
                git(
                    url: "${GIT_REPO}",
                    branch: "${BRANCH}",
                    credentialsId: "${GIT_CRED}"
                )
            }
        }

        
         stage('Build WAR') {
            steps {
        dir('my-webapp') {
            sh 'mvn -B clean package'
        }
    }
}
}
}
