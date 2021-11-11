pipeline {
    agent none
    environment {
        JENKINS_ACCESS_KEY = credentials('jenkins')
    }
    stages {
        stage("pre"){
            agent { docker 'maven:3.8.1-adoptopenjdk-11' }
            steps {
                echo "Hello, world!"
            }
        }
        stage("body"){
            agent { docker 'maven:3.8.1-adoptopenjdk-11' }
            steps{
                echo "Here we go~"
            }
        }
        stage("post"){
            agent { docker 'maven:3.8.1-adoptopenjdk-11' }
            steps{
                echo "We are finished!"
                sh 'printenv'
            }
        }
    }
}
