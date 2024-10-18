pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Specify the credentials ID
                git branch: 'main', url: 'git@github.com:Abhi03-tech/jenkins-ci-cd-bash.git', credentialsId: 'your-credentials-id'
            }
        }

        stage('Run Script') {
            steps {
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
