pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Budowanie aplikacji...'
                sh 'echo "Symulacja procesu budowania"'
                sh 'sleep 2'
            }
        }
        stage('Test') {
            steps {
                echo 'Uruchamianie testów jednostkowych...'
                sh 'echo "Symulacja testow zakończona sukcesem"'
                sh 'sleep 2'
            }
        }
        stage('Deploy to Test') {
            steps {
                echo 'Wdrażanie aplikacji do środowiska testowego...'
                sh 'echo "Aplikacja wdrozona na serwer testowy"'
            }
        }
    }
}