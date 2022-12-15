pipeline{
    agent any
    tools {
        maven 'Maven 3.8.6'
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