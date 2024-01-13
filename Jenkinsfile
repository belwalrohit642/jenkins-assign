pipeline {
    agent any

    stages {
        stage('Create New Branch') {
            steps {
                script {
                    // Replace 'new-branch' with your desired branch name
                    def newBranch = 'new-ew34'

                    // Create a new branch
                    sh "git checkout -b $newBranch"
                    sh "git push origin $newBranch"
                }
            }
        }
    }
}
