pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script{
                    sh 'git clone https://github.com/Chamathka-Rush/nginx-website.git'
                    echo 'cloned the repository...'
                    sh "pwd" 
                    sh "ls -lh"
                    
                }
            }
        }
        
        stage('Setting the directory'){
            steps{
                script{
                    dir('/var/jenkins_home/workspace/test/'){
                        sh "pwd"
                    }
                }
            }
        }
        
        stage('Build the docker image'){
            steps{
                script{
                    dir("/var/jenkins_home/workspace/test/") {
                        sh "pwd"
                        sh "docker build -t nginx-website:demo1 ."
                        sh "docker images"
                    }
                }
            }
        }
    }
}
