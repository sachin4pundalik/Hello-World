pipeline{
	agent any
		stages{

			stage('Build') {
			    steps {
				compileJava
			    }
			}

			stage('Test') {
			    steps {
				test
			    }
			}
		      }	

}
