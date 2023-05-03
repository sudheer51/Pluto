pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World    '
            }
        }
         stage('Ping') {
            steps {
               bat '''dir
               ping 127.0.0.1 -n 5'''
            }
        }
         stage('Execute Selenium tests') {
            steps {
               git 'https://github.com/sudheer51/Pluto.git'
               dir('mmppluto') {
                   bat 'mvn clean test'
                }
            }
        }
    }
}
