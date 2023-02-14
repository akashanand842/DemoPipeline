pipeline {
    agent any

    stages {
        stage('Git') {
 
                // Get some code from a GitHub repository
                git 'https://github.com/akashanand842/DemoPipeline.git'
        
        }
        stage('Maven Build'){
          
                def mvnHome = tool name: 'mvn', type: 'maven'
                sh "${mvnHome}/bin/mvn clean install"
          
        }
        stage('Run'){
     
                sh 'java -jar target/*jar-with-dependencies.jar'
            
           
        }
    }
}
