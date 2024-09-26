pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'make'
                        
                        stage('Permissions') {
                            steps {
                                script {
                                    sh 'chmod +x StringInverser.c' 
                                }
                            }
                        }
                        
                        stage('Nettoyage') {
                            steps {
                                sh 'make clean'
                            }
                        }
                    } else {
                        bat 'make'
                        
                        stage('Nettoyage') {
                            steps {
                                bat 'make clean'
                            }
                        }
                    }
                }
            }
        }
    }
}
