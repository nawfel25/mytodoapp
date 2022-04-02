pipeline {
    agent any

    stages {
        stage('npm install') {
            steps {sh "npm install"
                echo 'ess..'
            }
        }
        stage('run') { 
            steps{sh "ng serve &> /dev/null &"
                echo 'run..'
                }
        }
        stage('Test') {
            steps {sh "curl http://localhost:4200"
                echo 'Testing..'
            }
        }
       
        }
    }

