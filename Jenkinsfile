pipeline {
    agent any

    stages {
        stage('Vaidation') {
            steps {
                echo 'Validate Project..'
		sh 'mvn validate'
		sh 'mvn compile'
            }
        }
        stage('UnitTest') {
            steps {
                echo 'Testing..'
		sh 'mvn test'
            }
        }
        stage('SonarAnalysis') {
            steps {
                echo 'Sonar Analysis....'
		sh 'mvn sonar:sonar  -Dsonar.host.url=http://3.94.195.79:9000  -Dsonar.login=d9f50b08881ad2c42e91d2d02ae8f6f160a6fff4'
            }
        }
    }
}
