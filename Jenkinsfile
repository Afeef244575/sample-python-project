pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Afeef244575/sample-python-project.git'
            }
        }
        stage('Install Dependencies') {
            steps {
		sh 'python3 -m pip install --upgrade pip'
                sh 'pip3 install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'python3 -m unittest discover tests'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution complete!'
        }
    }
}
