pipeline {
    agent any
    stages {
       stage('Start') {
            steps {
                echo 'Hello, Start'
            }
        }
       stage('Clone') {
            steps {
                git url: 'https://github.com/softservedata/devopscc2026.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn -B package -DskipTests'
            }
        }
        stage('Unit Test') {
            steps {
                sh 'mvn -B test'
            }
        }
        stage('Done') {
            steps {
                echo 'Finish'
            }
        }
    }
}
