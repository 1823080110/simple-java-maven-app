pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
	            bat 'D:'
	            bat 'cd D:/ruanjian/workspace/s'
                bat 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}
