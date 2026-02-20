pipeline {
    agent any

    stages {
	stage('Checkout') {
            steps {
		echo 'Checking out code...'
		checkout scm
	    }
	}

	stage('Build') {
	    steps {
		echo 'Building application'
		sh 'echo "Build step placeholder"'
	    }
	}

	stage('Test') {
	    steps {
		echo 'Deploying...'
		sh 'echo "Testing step placeholder"'
	    }
	}

	}
    post {
	success { 
	    echo 'Pipeline completed successfully'
	    }

	failure {
	    echo 'Pipeline failed'
	    }

	always {
	    echo 'Pipeline finished - cleaning up'
	    }

    }

	
}

