def app = 'Unknown'
pipeline {
    agent any
    stages {
        stage('build'){
            steps{
                script{
                    app = docker.build("pavansh/testrepo")
                    docker.withRegistry('', 'dockerhub wala'){
                        app.push("${env.BUILD_NUMBER}")
                    }
                }
            }
        }
    }  
}

