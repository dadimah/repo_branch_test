pipeline {
    agent any
    
    stages {
        stage('Extract Server Name') {
            steps {
                script {
                    def branchName = env.BRANCH_NAME ?: ''
                    def tokens = branchName.tokenize('/')
                    def server = ''
                    if (tokens.size() > 1) {
                        tokens = tokens.get(1).tokenize('-')
                        if (tokens.size() > 2) {
                            server = tokens.get(2)
                        }
                    }
                    echo "Server Name: ${server}"
                }
            }
        }
    }
}
