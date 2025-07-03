pipeline {
    agent any               // Run on the built-in worker (the Jenkins container)
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/<your-user>/hello-jenkins.git'
            }
        }
        stage('Run script') {
            steps {
                sh 'chmod +x hello.sh && ./hello.sh'
            }
        }
    }
    post {
        success { echo '🎉  Build finished OK' }
        failure { echo '💥  Build failed'     }
    }
}
