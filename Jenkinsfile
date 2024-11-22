pipeline {
    agent any

    stages {
        stage('Job 1: Clone GitHub Repository') {
            steps {
                echo 'Cloning the GitHub repository...'
                git url: 'https://github.com/Mokshithanaidu/example.git'
            }
        }

        stage('Job 2: Execute Java Program') {
            steps {
                echo 'Navigating to week-4 and running the Java program...'
                script {
                    sh '''
                    cd week-4
                    javac HelloJava.java
                    java HelloJava
                    '''
                }
            }
        }

        stage('Job 3: Execute Python Script') {
            steps {
                echo 'Navigating to week-4 and running the Python script...'
                script {
                    sh '''
                    cd week-4
                    python3 hellopy.py
                    '''
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
