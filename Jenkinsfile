pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/UsmanEjaz22/DoMidsLabExam2.git' // Use this if the job isn't configured to correctly pull from Git
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'No dependencies to install for a static HTML site.'
            }
        }

        stage('Run Tests') {
            steps {
                // Mock HTML validation test
                sh 'echo "Running HTML validation..."'
                sh 'exit 0' // Simulate a successful test
                // Can replace with actual HTML validation tools like htmlhint or pa11y
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '**/*', fingerprint: true
            }
        }
    }
}