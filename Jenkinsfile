pipeline {
    agent any
    
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'release_EXO_1.29.0_DEV', url: 'https://github.com/dadimah/repo_branch_test.git'
            }
        }
        
        stage('Extract Server Name') {
            steps {
                script {
                    def branchName = env.BRANCH_NAME ?: ''
                    def server = branchName.tokenize('/').get(1).tokenize('-').get(2)
                    echo "Server Name: ${server}"
                }
            }
        }
    }
}
