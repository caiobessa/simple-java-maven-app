pipeline {
    agent any
    stages {
        stage('Clean up') {
            steps {
                deleteDir()
            }
        }
        stage('Clone Repo') {
            steps {
                sh 'git clone https://github.com/jenkins-docs/simple-java-maven-app'
            }
        }
        stage('Build') {
            steps {
                dir('simple-java-maven-app') {
                    sh 'maven clean install'
                }
            }
        }
        stage('Test') {
            steps {
                dir('simple-java-maven-app') {
                    sh 'maven test'
                }
            }
        }
    }
}
