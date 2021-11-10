pipeline {
    agent {
        docker {
            image 'busybox'
            label 'latest'
        }
    }
    stages {
        stage("pre"){
            steps {
                echo "Hello, world!"
            }
        }
        stage("body"){
            steps{
                echo "Here we go~"
            }
        }
        stage("post"){
            steps{
                echo "We are finished!"
            }
        }
    }
}
