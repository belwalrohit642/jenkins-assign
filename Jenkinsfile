pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout the repository
                    checkout scm
                }
            }
        }

        stage('Create Branch') {
            steps {
                script {
                    // Define the new branch name
                    def newBranch = 'your_nsdsdessdsw_branch_name'

                    // Create a new branch
                    sh "git checkout -b ${newBranch}"

                    // Push the new branch to GitHub
                    sh "git push origin ${newBranch}:${newBranch}"
                }
            }
        }
    }
}
