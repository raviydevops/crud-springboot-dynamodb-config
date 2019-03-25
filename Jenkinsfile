pipeline {
    agent any
    stages {
        stage ('git-clone') {
            steps {
                echo "Deploying to eternal from ephermeral..."
                build job: "config-multibranch-test/local", propagate: true, wait: true
            }
        }
    }
}
