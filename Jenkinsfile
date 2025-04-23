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
                reportDir: '', // Directory containing HTML reports
                reportFiles: 'index.html',         // The HTML file to publish
                reportName: 'My HTML Report',      // Name of the HTML report
                keepAll: true,                     // Whether to keep all previous reports
                alwaysLinkToLastBuild: true        // Whether to link to the last build report
            ])
        }
    }
}
