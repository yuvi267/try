def app = 'Unknown'
pipeline {
    agent any
    stages {
        stage('build'){
            steps{
                script{
                    app = docker.build("yuvi267/try")
                }
            }
        }
    }  
}
