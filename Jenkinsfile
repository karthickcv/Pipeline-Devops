pipeline{
    agent none
    environment {
        DEPLOY_TO='dev'
    }
    stages {
        stage('Build') {
            agent {
                label "Slave 1"
            }
            when {
                beforeAgent false
                environment name: 'DEPLOY_TO' , value: 'production'
            }
            steps {
                echo "Building....."
            }
        }
    }
}