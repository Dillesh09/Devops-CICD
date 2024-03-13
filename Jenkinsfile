pipeline {
    agent any
    tools{
	    maven 'Maven'		
	}
   

    stages {
        stage('git-checkout') {
            steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/Dillesh09/Devops-CICD.git'
            }
        }
        
        stage('Code-Compile') {
            steps {
               sh "mvn clean compile"
            }
        }
        
       	
	
        stage('Code-Build') {
            steps {
               sh "mvn clean install"
            }
        }
       
        
    }
}
