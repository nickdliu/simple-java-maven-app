pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
			args '-v /root/.m2:/root/.m2'
			/*args '-v d:\\home\\.m2:/var/run/docker.sock'*/
            /*args '-v d:\\home\\.m2:/root/.m2' */
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}