pipeline {
    agent any

    stages {
        stage('npm install') {
            steps {sh "npm install"
                echo 'ess..'
            }
        }
        stage('run') { 
            steps{script{
                withEnv(['JENKINS_NODE_COOKIE=dontkill']) {
                     sh "ng serve &"
                }
            }
               
                }
        }
        stage('Test') {
            steps {sh "curl http://localhost:4200"
                echo 'Testing..'
            }
        }
       
        }
    }

