pipeline {
    agent any  // You can also specify a Windows-specific agent label if needed, e.g., agent { label 'windows' }
    stages {
        stage('Restore') {
            steps {
                // Restore NuGet packages
                bat 'dotnet restore'
            }
        }
        stage('Build') {
            steps {
                // Build the project (using Release configuration; adjust if needed)
                bat 'dotnet build --configuration Release'
            }
        }
        stage('Test') {
            steps {
                // Run unit tests
                bat 'dotnet test'
            }
        }
    }
}
