#!groovy

pipeline {
    agent any
	environment {
		PATH="C:\Program Files\Git\usr\bin:$path"
	}
	
    tools {
        maven 'Maven 3.8.1' // You need to add a maven with name "3.6.0" in the Global Tools Configuration page

    }

    stages {
        stage("Build") {
            steps {
			echo 'this is minimal pipeline.'
                sh "mvn -version"
                sh "mvn clean install"
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}
