pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/alvarotarrifaste/automationTestingJava.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Run') {
            steps {
                bat 'java -cp target/classes com.automation.testig.App'
            }
        }
    }
}
