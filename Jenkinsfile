pipeline {
    agent any

    stages {
        stage('Remove Old Clone') {
            steps {
                // Remove the existing clone
                deleteDir()
            }
        }
        stage('Clone') {
            steps {
                // Cloning the GitHub repository
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/alinashah56/jkhk.git']]])
            }
        }
        stage('Build') {
            steps {
                // Your build steps here
                bat 'app.js' // Example build step
            }
        }
    }
}
