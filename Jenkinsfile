pipeline {
	agent any
	stages{
		stage('validate'){
			steps {
				echo "validate pipeline"
				sh "mvn validate"
			}
		}
		stage('compile'){
			steps{
				echo "compile pipeline"
				sh "mvn compile"
			}
		}
		stage('Unit test'){
			steps{
				echo "unit test case"
				sh "mvn test"
			}
		}
	}
}
