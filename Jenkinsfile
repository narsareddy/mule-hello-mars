pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Build: step 1"'
                sh '''
                    echo "Build: step 2.1"
                    pwd
                    '''
            }
        }
        stage('Test') {
            steps {
                sh 'mvn --version'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploy: step 1"'
                sh 'echo "Deploy: step 2"'
            }
        }
    }
}
