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
    post {
        always {
            publishHTML([
                reportDir: '',                 // No subdirectory, index.html is in the root
                reportFiles: 'index.html',     // The HTML file to publish
                reportName: 'My HTML Report',  // Name of the HTML report
                keepAll: true,                 // Keep all previous reports
                alwaysLinkToLastBuild: true,   // Link to the last build report
                allowMissing: true              // Allow the build to proceed if the report is missing
            ])
        }
    }
}
