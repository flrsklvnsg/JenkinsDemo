pipeline {
    agent any

    stages {
        stage('Test Hello') {
            steps {
                echo 'Test Hello World'
            }
        }
        stage('Build') {
            steps {
                echo 'Building'
           //     sh 'npm install'
            //    sh 'npm build'
            }
        }
            stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
        stage('Release') {
            steps {
                echo 'Releasing'
            }
       
        }
        stage('Checkout') {
            steps {
                echo 'Checkout'
            }
       
        }
        stage('Cleanup') {
            steps {
                echo 'Cleanup'
            }
       
        }
    }
}
    
