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
                dir('ex1spring') {
                    sh 'mvn clean install'
                    sh 'docker build -t dockerexp1.spring .'
                }
            }
        }

        stage("Run docker compose") {
            steps {
                dir('ex1spring') {
                    sh 'docker compose up -d'
                }
            }
        }
    }
}
