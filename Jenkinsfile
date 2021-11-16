pipeline {
    agent none
    environment {
        JENKINS_ACCESS_KEY = credentials('5ec6d6d2-563a-4822-9775-d50f1e565101')
    }
    stages {
        input {
            message "Shall we go?"
            ok "yes"
            parameters {
                string(name: 'Go or No go', defaultValue: 'Let's process', description: 'do you approval it?')
    }  
}
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
                sh "printenv"
                sh "echo $JENKINS_ACCESS_KEY_USR"
                sh "echo $JENKINS_ACCESS_KEY_PSW"
            }
        }
    }
}
