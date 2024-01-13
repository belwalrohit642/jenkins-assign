pipeline {
    agent any

    environment {
        GITHUB_REPO = 'belwalrohit642/jenkins-assign'
        NEW_BRANCH_NAME = 'new-brasdsdnch'
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout([$class: 'GitSCM', 
                              branches: [[name: 'master']], 
                              userRemoteConfigs: [[url: "https://github.com/${GITHUB_REPO}.git"]]])
                }
            }
        }

        stage('Create Branch') {
            steps {
                script {
                    withCredentials([usernamePassword(credentialsId: 'rahul_github_cred', passwordVariable: 'GITHUB_PASSWORD', usernameVariable: 'GITHUB_USERNAME')]) {
                        sh "git checkout -b ${NEW_BRANCH_NAME}"
                        sh "git push origin ${NEW_BRANCH_NAME}"
                    }
                }
            }
        }
    }
}
