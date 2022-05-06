def gv

pipeline {
    agent any
    parameters{
        string(name: 'VERSION', defaultValue: '', description: 'version to deploy on prod')
        choice(name: 'VERSION', choices: ['1.1.0','1.2.0','1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {
         stage('init') {
            steps {
                script{
                    gv = load "script.groovy"

                }
            }
        }
        stage('Build') {
            steps {
                script{
                    gv.buildApp()
                } 

            }
        }
            stage('Test') {
            steps {
                when{
                    expression{
                        params.executeTests
                    }
                }
                 script{
                    gv.testApp()
                } 
            }
        }
        stage('Deploy') {
            steps {
                script{
                    gv.deployApp()
                } 
                }
        }
        
    }
}
    
