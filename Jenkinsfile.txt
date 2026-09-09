pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/mokshitha31vs-mok/build3.git'
            }
        }

        stage('Build') {
            steps {
                bat '"C:/Users/MOKSHITHA/AppData/Local/Programs/Python/Python311/python.exe" app.py'
            }
        }
    }
}