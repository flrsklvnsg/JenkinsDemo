pipeline {
    agent any
    parameters{
        string(name: 'VERSION', defaultValue: '', description: 'version to deploy on prod')
        choice(name: 'VERSION', choices: ['1.1.0','1.2.0','1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {
        stage('Test Hello') {
            steps {
                echo 'Test Hello World'
            }
        }
        stage('Build') {
            steps {
                echo'Building' 

            }
        }
            stage('Test') {
            steps {
                when{
                    expression{
                        params.executeTests
                    }
                }
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'   
                echo "deploying version ${params.VERSION}"
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
    
