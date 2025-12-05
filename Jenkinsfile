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
        bat 'javac -d build src/main/java/com/automation/testig/*.java'
      }
    }

    stage('Run') {
      steps {
        bat 'java -cp build com.automation.testig.App'
      }
    }
  }
}
