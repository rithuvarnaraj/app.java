stage('Build Docker Image') {
    steps {
        script {
            sh 'docker build -t rithuvarnaraj/jenkins-demo:latest .'
        }
    }
}

stage('Login to Docker Hub') {
    steps {
        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
    }
}

stage('Push Image to Docker Hub') {
    steps {
        sh 'docker push rithuvarnaraj/jenkins-demo:latest'
    }
}
