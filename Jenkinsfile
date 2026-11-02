pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Pobranie kodu z repozytorium Git
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Budowanie aplikacji...'
                sh 'mvn clean compile' // lub np. 'npm install' dla Node.js
            }
        }
        stage('Test') {
            steps {
                echo 'Uruchamianie testów jednostkowych...'
                sh 'mvn test' // lub 'npm test'
            }
        }
        stage('Deploy to Test') {
            steps {
                echo 'Wdrażanie aplikacji do środowiska testowego...'
                sh './deploy-test.sh' // skrypt wdrażający
            }
        }
    }
}