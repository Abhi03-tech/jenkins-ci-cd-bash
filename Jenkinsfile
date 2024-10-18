pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Use the SSH URL for the repository
                git branch: 'main', url: 'git@github.com:Abhi03-tech/jenkins-ci-cd-bash.git'
            }
        }

        stage('Run Script') {
            steps {
                // Replace script.sh with your script name
                sh './script.sh'
            }
            steps {
                sh './new_script.sh'}
        }
    }
}
