pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch:'master',url:'https://github.com/RANI921/Q1.git'
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean package'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('Run Application'){
			steps{
				sh 'java -jar target/MY_MAVEN-1.0-SNAPSHOT.jar'
			}
		}
	}
	post{
		success{
			echo "Successfull"
		}
		failure{
			echo "Failure"
		}
	}
}
