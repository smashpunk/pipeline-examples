pipeline {
    agent none
    environment {
        JENKINS_ACCESS_KEY = credentials('a4d39934-9d2c-4594-b866-748e58becfea')
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
                sh 'echo $JENKINS_ACCESS_KEY_USR'
                sh 'echo $JENKINS_ACCESS_KEY_PSW'
            }
        }
    }
}
