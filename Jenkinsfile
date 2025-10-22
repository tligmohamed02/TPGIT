pipeline {
    agent any
    tools {
        jdk 'JDK21'
    }
    stages {
        stage('Checkout code') {
            steps {
                git branch: 'master', url: 'https://github.com/tligmohamed02/TPGIT.git'
            }
        }
        stage('Compile code' ) {
            steps {
                sh 'javac -d out src/main/java/net/mohamed/Main.java'
            }
        }
        stage('Execute code') {
            steps {
                sh 'java -cp out net.mohamed.Main'
            }
        }
        stage('display message webhook'){
            steps {
                sh 'echo hello from Github'
            }
        }
    }
}
