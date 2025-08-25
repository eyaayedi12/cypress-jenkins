pipeline{
    agent {
        docker{
            image "cypress/browsers:latest" 
        }
    }
    stages{
        stage('test stage1'){
            steps{
                echo 'hello from jenkinsfile'
                sh 'npx cypress run --browser chrome'
            }

        }
        stage('add-stage'){
            steps{
                echo 'hello from second stage'
            }
        }
    }
}