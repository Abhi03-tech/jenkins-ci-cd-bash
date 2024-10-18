pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Use the SSH URL for the repository
                git 'git@github.com:Abhi03-tech/jenkins-ci-cd-bash.git'
            }
        }

        stage('Run Script') {
            steps {
                // Replace script.sh with your script name
                sh './script.sh'
            }
        }

        stage('Push Changes') {
            steps {
                sh '''
                echo "New content" >> script.sh
                git add script.sh
                git commit -m "Updated script"
                git push origin main
                '''
            }
        }
    }
}

