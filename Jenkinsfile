pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ankitamohanty1509/python.git'  
            }
        }
        stage('Install Dependencies') {
            steps {
                script {
                    sh 'pip install -r requirements.txt'
                }
            }
        }
        stage('Run Tests') {
            steps {
                script {
                    sh 'pytest test_app.py'
                }
            }
        }
    }
}
