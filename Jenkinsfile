pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/ankitamohanty1509/python.git', branch: 'main'
            }
        }
        stage('Install Dependencies') {
            steps {
                script {
                    
                    sh 'python3 -m venv venv'

                    sh '. venv/bin/activate && pip install -r requirements.txt'
                }
            }
        }
        stage('Run Tests') {
            steps {
                script {
                    
                    sh '. venv/bin/activate && pytest test_app.py'
                }
            }
        }
    }
}
