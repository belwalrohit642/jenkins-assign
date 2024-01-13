pipeline {
    agent any

    stages {
        stage('Create New Branch') {
            steps {
                script {
                    // Replace 'new-branch' with your desired branch name
                    def newBranch = 'new-e221w34'

                    // Set the GitHub credentials ID
                    def credentialsId = 'github_cred'

                    // Create a new branch
                    sh "git checkout -b $newBranch"
                    sh "git push origin $newBranch"
                }
            }
        }
    }
}
