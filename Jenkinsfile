pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main', url:'https://github.com/Summi1610/jenkinsdemo.git'
            }
        }

        stage('Build (Optional)') {
            steps {
                echo "No build required for HTML file"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying index.html to Apache server..."
                sh '''
                sudo cp index.html /var/www/html/
                '''
            }
        }

    }

    post {
        success {
            echo "Deployment Successful ✅"
        }
        failure {
            echo "Deployment Failed ❌"
        }
    }
}
