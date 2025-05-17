pipeline {
    agent any

    tools {
        maven 'maven'
    }

    stages {
        stage("Clean up") {
            steps {
                deleteDir()
            }
        }

        stage("Clone repo") {
            steps {
                sh 'git clone https://github.com/Sihem8/ex1spring.git'
            }
        }

        stage("Generate backend image") {
            steps {
                dir('exp1-spring') {
                    sh 'mvn

