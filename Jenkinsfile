pipeline {
    agent any
    stages {
        stage ('git-clone') {
            steps {
                echo "Deploying to eternal from ephermeral..."
                build 'config-multibranch-test'
            }
        }
    }
}
