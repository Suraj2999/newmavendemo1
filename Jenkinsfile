#!groovy

pipeline {
    agent any
	
    tools {
        maven 'Maven 3.8.1' // You need to add a maven with name "3.6.0" in the Global Tools Configuration page

    }

    stages {
        stage("Build") {
            steps {
			echo 'this is minimal pipeline.'
               // bat "mvn -version"
               // bat "mvn clean install"
		//bat "cd F:\my-app\src\main\java\com\mycompany\app"
		   bat "java App"
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}
