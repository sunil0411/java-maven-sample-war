pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
		stage('Clone Project') {
            steps {
               git 'https://github.com/shyampandu/java-maven-sample-war.git'		   
			  
            }
        }
		
		stage('Build') {
            steps {
                sh "git --version"
				sh "java -version"
				
            }
        }
		stage('Clean') {
            steps {
                sh "mvn clean"
		 
            }
        }
		stage('Compile') {
            steps {
                sh "mvn compile"
            }
        }
		stage('Package') {
            steps {
                sh "mvn package"
		cleanWs()
            }
        }
    }
}
