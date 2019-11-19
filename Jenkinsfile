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
		dockerbuild -t= "jackfarr2094/simple-project:latest" .
		echo "Build"
                }
            }
        stage('Deploy') {
            steps {
		echo "Execute Order 66"
            }
        }
    }
}

