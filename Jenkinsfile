
pipeline {
    agent {
     docker {
        image 'ubuntu:14.04'
    }

    }
    stages {
        stage('Build') {
            steps {
                echo 'BuSSSilding..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'ls'
            }
        }
    }
}
