pipeline {
    agent any

    stages {

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
