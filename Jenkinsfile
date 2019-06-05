pipeline {
    agent any;
    stages {
        stage('CleanUp'){
            steps{
                cleanWs();
            }   
        }
        stage('Checkout SCM'){
            steps {
                checkout scm;
            }
        }
        stage('Build Stage') {
            steps {
                sh 'chmod +x app.sh'
                sh 'sh app.sh'
            }
        }
        stage('Testing Stage') {
            steps {
                sh 'echo HelloWorld'
            }
        }
        stage('Deploy Stage') {
            steps {
                sh 'echo HelloWorld'
            }
        }
    }
}
