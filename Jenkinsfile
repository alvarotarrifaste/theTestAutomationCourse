pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/alvarotarrifaste/automationTestingJava.git', branch: 'main'
            }
        }

        stage('Compile') {
            steps {
                bat 'javac src\\Main.java'
            }
        }

        stage('Run') {
            steps {
                bat 'java -cp src Main'
            }
        }
    }
}
