pipeline { 
    agent any 
    tools { 
        maven 'Maven' // Ensure name matches configured Maven installation 
    } 
    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'master', url: 'https://github.com/KRISHNA-MS17/jenkinspipeline.git'  
            } 
        } 
        stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
        } 
        stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
        } 
        stage('Run Application') {  
            steps { 
                bat 'java -jar target/jenkinspipeline-0.0.1-SNAPSHOT.jar'  
            } 
        } 
    } 
}

