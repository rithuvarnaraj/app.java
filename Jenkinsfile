pipeline {
    agent any

    tools {
        // Make sure that Maven is installed in Jenkins. You can install it and specify the name here.
        maven 'buildmaven'
    }


    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from Git or any other SCM
                git 'https://github.com/rithuvarnaraj/app.java/'
            }
        }

        stage('Build') {
            steps {
                script {
                    // Run Maven to build the project
                    sh 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run tests using Maven
                    sh 'mvn test'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Optional: Deploy your application (e.g., to a server)
                    echo "Deploying the application..."
                }
            }
        }
    }

    post {
        always {
            // Actions that will always be run after the pipeline finishes
            echo "Pipeline execution complete."
        }
    }
}
