pipeline {
    agent none
    environment {
        JENKINS_ACCESS_KEY = credentials('91d1f909-2331-4e64-8218-6f6e6502f251')
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
