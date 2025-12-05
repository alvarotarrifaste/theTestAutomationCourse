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
                bat '''
                    if not exist build mkdir build
                    forfiles /p javaproject\\src\\main\\java /s /m *.java /c "cmd /c javac -d build @path"
                '''
            }
        }

        stage('Run') {
            steps {
                bat 'java -cp build com.automation.testig.App'
            }
        }
    }
}
