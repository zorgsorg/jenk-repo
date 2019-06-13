pipeline {
    agent any

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
            }
        }
    }

    post {
        success {
            script {
                githubPRComment comment: githubPRMessage('Build ${BUILD_NUMBER} ${BUILD_STATUS}')
                 if (env.CHANGE_ID) {
                                         pullRequest.addLabel('Build Failed')
                }
            }
        }
    }
}
