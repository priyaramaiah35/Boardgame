pipeline {
    agent any
    
    tools {
        maven 'Maven'
        jdk 'JDK17'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', changelog: true, poll: true, url: 'https://github.com/priyaramaiah35/Boardgame.git'
            }
        }
        stage('Compile') {
            steps {
             sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
               sh 'mvn package'
            }
        }
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
