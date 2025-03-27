pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/ankitamohanty1509/python.git', branch: 'main'
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
