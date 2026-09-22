pipeline {
    agent any
        stages {
        stage ('check'){
            steps{
                git 'https://github.com/KeittoKeisari21/cal_3014_demo.git'
            }
        }
        stage ('build'){
            steps{
                bat 'mvn clean install'
            }
        }

        stage('test') {
            steps{
                bat 'mvn test'
            }
        }
        stage('jacoco'){
            steps{
                jacoco()
            }
        }

    }
}