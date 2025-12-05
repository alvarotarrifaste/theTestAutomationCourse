pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                bat 'javac src\\main\\java\\*.java'
            }
        }

        stage('Run') {
            steps {
                bat 'java -cp src\\main\\java Main'
            }
        }
    }
}
