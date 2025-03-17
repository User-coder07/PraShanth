pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/User-coder07/PraShanth.git'  // Updated repo URL
            }
        }

        stage('Compile Java Code') {
            steps {
                bat 'javac HelloWorld.java'
            }
        }

        stage('Run Java Program') {
            steps {
                bat 'java HelloWorld'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '**\\*.class', fingerprint: true
            }
        }
    }
}
