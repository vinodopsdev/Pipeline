pipeline{
    agent any
    stages{
        stage("Create Folder"){
            steps{
                sh "mkdir -p ${env.JOB_NAME}"
            }
        }
        stage("Maven Build"){
            steps{
                sh 'mvn clean package'
            }
        }
        stage("Deploy to Tomcat Dev"){
            steps{
                tomcatDeploy('tomcat-dev','ubuntu','13.233.84.204')
            }
        }
    }
}
