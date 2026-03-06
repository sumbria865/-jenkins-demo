pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh '''
                echo "Building Java project..."
                ls
                javac Hello.java
                '''
            }
        }

        stage('Run') {
            steps {
                sh '''
                echo "Running Java program..."
                java Hello
                '''
            }
        }

    }

    post {
        success {
            echo "Pipeline executed successfully!"
        }
        failure {
            echo "Pipeline failed!"
        }
    }
}
