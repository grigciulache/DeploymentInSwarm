pipeline{

    environment {
        registry = "grigciulache/httpd"
        registryCredential = 'dockerhub'
        projectGit='https://github.com/grigciulache/DeploymentInSwarm.git'
    } 
    agent any
    stages{
        stage("Git clone"){
            steps{
                echo 'Git clone'
                git projectGit
            }
        }
        
        stage('Run Application'){
            steps{
                    sh label: '', script: 'sudo chmod 777 deployment.sh'
                    sh label: '', script: './deployment.sh'
                    //test
            }
        }
    }
}
