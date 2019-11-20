pipeline {
    agent any

    stages {
        stage('Testing Environment') {
            steps {
                    sh 'mvn test -Dtest=ControllerAndServiceSuite'
		    sh 'mvn test -Dtest=IntegrationSuite'
                }
            }
        stage('Build') {
          steps {
		sh 'mvn package -DskipTests'
		sh 'docker build --tag= "jackfarr2094/simple-project:latest"' .
		echo "Build"
                }
            }
        stage('Deploy') {
            steps {
		sh 'docker push jackfarr2094/simple-project:latest'
		echo "Execute Order 66"
            }
        }
	  stage('Testing Environment') {
            steps {
                echo "hello"
            }
        }
      stage('Staging') {
            steps {
                echo "hello"
            }
        }
      stage('Production') {
            steps {
                echo "hello"
            }
        }
    }
}

