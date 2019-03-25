pipeline {
    agent any
    stages {
        stage ('git-clone') {
            steps {
                echo "Deploying to eternal from ephermeral..."
                script {
                    def environmnetsToDeploy = ['local', 'local_and_aws', 'aws_cdk']
                    environmnetsToDeploy.each {
                        build job: "config-multibranch-test/$it", propagate: true, wait: true
                    }
                }
            }
        }
    }
}
