pipeline{
    agent {
    	docker{
	        image "openjdk:11-ea-jdk-slim"
    	}
    }

    stages{
        stage("Build"){
            steps{
                echo "========executing Build========"
                sh "mvn -version"
                sh "mvn clean install"
            }
        }
        stage("Build Image"){
            steps{
                echo "========executing Build Images========"
               	sh "docker build -t java11 ."
            }
        }
    }
}

