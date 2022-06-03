pipeline {
    agent {
        label 'demo'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                build 'seleniumMaven'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        always{
            echo "TimeStamp: ${currentBuild.startTimeInMillis}"
            echo 'Pipeline Done!!!'
        }
    }
}
