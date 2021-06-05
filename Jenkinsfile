pipeline {
    agent any

    stages {
        stage('clone and clean') {
            steps {
                sh 'git clone https://github.com/venkatcope/my-app'
		sh 'mvn clean'
            }
        }
        stage('Test') {
            steps {
              	sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
