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
		printMessage("checkout branch [${env.BRANCH_NAME}]")
                sh 'echo checkout OK'
            }
        }
        stage('Build Stage') {
            steps {
                sh 'chmod +x app.sh'
                sh 'sh app.sh'
                sh 'echo Build OK'
            }
        }
        stage('Testing Stage') {
            steps {
                sh 'echo Testing'
            }
        }
        stage('Deploy Stage') {
            steps {
                sh 'echo Deploy'
            }
        }
    }
}
