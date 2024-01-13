pipeline {
    agent any

    environment {
        NEW_BRANCH_NAME = 'new-bderranch'
    }

    stages {
        stage('Create New Branch') {
            steps {
                withCredentials([usernamePassword(credentialsId: '53bc091f-05d7-42fa-a824-680feef7cb22', passwordVariable: 'GIT_PASSWORD', usernameVariable: 'GIT_USERNAME')]) {
                    // Checkout the repository with SCM configuration
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/belwalrohit642/jenkins-assign.git']]])

                    // Create a new branch
                    sh "git checkout -b ${NEW_BRANCH_NAME}"
                    sh "git push origin ${NEW_BRANCH_NAME}"
                }
            }
        }
    }
}
