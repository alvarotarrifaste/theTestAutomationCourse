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
        sh 'javac src/Main.java'
      }
    }
    stage('Run') {
      steps {
        sh 'java -cp src Main'
      }
    }
  }
}
