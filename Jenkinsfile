pipeline{
	agent any
		stages{

			stage('Build') {
			    steps {
				sh 'make' (1)
				archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true (2)
			    }
			}

			stage('Test') {
			    steps {
				/* `make check` returns non-zero on test failures,
				* using `true` to allow the Pipeline to continue nonetheless
				*/
				sh 'make check || true' (1)
				junit '**/target/*.xml' (2)
			    }
			}
		      }	

}
