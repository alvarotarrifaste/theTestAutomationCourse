pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                bat '''for %%f in (src\\main\\java\\*.java) do javac "%%f"'''
            }
        }

        stage('Run') {
            steps {
                bat 'java -cp src/main/java Main'
            }
        }
    }
}
