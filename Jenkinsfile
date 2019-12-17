pipeline {
    environment { 
    HTTP_PROXY = 'http://web-proxy.bbn.hpecorp.net:8080'
    }
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
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
