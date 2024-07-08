pipeline {
    agent any
    
    stages {
        stage('Hello') {
            steps {
                echo 'Hello, World!'
            }
        }
        
        stage('Cat README') {
            when {
		branch "dev-*"
            }
            steps {
                script {
                    if (fileExists('README.md')) {
                        sh 'cat README.md'
                    } else {
                        echo 'README file does not exist'
                    }
                }
            }
        }
    }
}

