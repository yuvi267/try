def app = 'Unknown'
pipeline {
    agent any
    stages {
        stage('build'){
            steps{
                script{
                    app = docker.build("yuvrajsingh/try")
                    docker.withRegistry('', 'dockerhub wala'){
                        app.push("${env.BUILD_NUMBER}")
                    }
                }
            }
        }
    }  
}

