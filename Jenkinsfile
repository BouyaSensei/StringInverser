pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'make'
                        
                        stage('Permissions') {
                          
                            sh 'chmod +x StringInverser.c' 
                        }
                        
                        stage('Nettoyage') {
                           
                            sh 'make clean'
                        }
                    } else {
                        bat 'make'
                        
                        stage('Nettoyage') {
                           
                            bat 'make clean'
                        }
                    }
                }
            }
        }
    }
}
