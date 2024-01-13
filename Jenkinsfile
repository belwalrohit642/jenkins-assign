pipeline {
    agent any

    environment {
        GIT_REPO_URL = 'https://github.com/belwalrohit642/jenkins-assign.git'
        NEW_BRANCH_NAME = 'new-branch'
    }

    stages {
        stage('Clone Repository') {
            steps {
                script {
                    // Clone the repository
                    git branch: 'master', credentialsId: '53bc091f-05d7-42fa-a824-680feef7cb22', url: GIT_REPO_URL
                }
            }
        }

        stage('Create New Branch') {
            steps {
                script {
                    // Create a new branch
                    sh "git checkout -b ${NEW_BRANCH_NAME}"
                    sh "git push origin ${NEW_BRANCH_NAME}"
                }
            }
        }
    }
}

