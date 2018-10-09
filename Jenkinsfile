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
                if (pullRequest.mergeable) {
                    pullRequest.merge([ commitMessage : 'merge commit message here'] )
                } else {
                    pullRequest.addLabel('No automerge')
                }
            }
        }
    }
}
