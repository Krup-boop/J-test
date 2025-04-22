pipeline {
    agent any
    stages {
        stage('Open HTML') {
            steps {
                echo 'Pipeline started for HTML!'
                bat 'start index.html'  // Windows
                // OR
                // sh 'xdg-open index.html'  // Linux
            }
        }
    }
}
