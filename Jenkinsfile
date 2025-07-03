pipeline {
    agent any
    stages {
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
