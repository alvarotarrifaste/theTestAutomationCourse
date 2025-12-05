pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/alvarotarrifaste/automationTestingJava.git'
            }
        }

        stage('Build') {
            steps {
                bat """
                    cd javaproject
                    mvn clean package
                """
            }
        }

        stage('Run') {
            steps {
                bat """
                    cd javaproject
                    mvn exec:java -Dexec.mainClass=com.automation.testig.App
                """
            }
        }
    }
}
