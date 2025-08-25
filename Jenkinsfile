pipeline{
    agent {
        docker{
            image "cypress/browsers:latest"
            args '--entrypoint=' 
        }
    }
    stages{
        stage('installer npm'){
            steps{
                echo 'installer '
                
                sh 'npm ci'
            }

        }
        stage('npm run '){
            steps{
                echo 'npm run'
                sh 'npx cypress run --browser edge'
            }
        }
        
    }
    post{
        always{
            archiveArtifacts artifacts: 'cypress/reports/**/*.*', followSymlinks: false
        }
    }
}