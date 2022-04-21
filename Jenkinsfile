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
		stage('cobertura generate report job'){
			steps{
				echo "cobertura report job"
				sh "mvn cobertura:cobertura -Dcobertura.report.format=xml"
				cobertura "**/target/site/cobertura/coverage.xml"
			}
		}
	}
}
