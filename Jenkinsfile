pipeline{
    agent any
    stages {
        stage('Clean') {
            steps {
                bat ''' 
                    rd /s /q testJenkins
                '''   
            }
        }
        stage('Clone') {
            steps{
                bat ''' 
                    git clone https://github.com/devgosset/testJenkins.git
                '''   
            }
        }
        stage('Build') {
            steps {
                bat '''
                    cd testJenkins/ && javac Main.java
                '''
            }
        }
        stage('Run'){
            steps{
                bat ''' 
                    cd testJenkins/ && java Main
                '''
            }
        }
    }
}
