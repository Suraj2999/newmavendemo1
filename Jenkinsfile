#!groovy

pipeline {
    agent any
	environment{
	Path = "F:\apache-maven-3.8.1\bin:$PATH"
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
