pipeline {
    agent any

    stages {
        stage('clone and clean') {
            steps {
		sh 'rm -rf my-app'
                sh 'git clone https://github.com/venkatcope/my-app'
		sh 'mvn clean'
            }
        }
        stage('Test') {
            steps {
		sh 'echo 'Testing starting'
              	sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
		sh 'package stating'
                sh 'mvn package'
            }
        }
    }
}
