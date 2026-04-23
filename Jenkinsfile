pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/YOUR_USERNAME/YOUR_REPO.git'
            }
        }

        stage('Build') {
            steps {
                echo "No build needed for static HTML"
            }
        }

        stage('Deploy to GitHub Pages') {
            steps {
                sh '''
                git config --global user.name "jenkins"
                git config --global user.email "jenkins@example.com"

                git checkout -B gh-pages
                git add .
                git commit -m "Deploy to GitHub Pages" || true
                git push origin gh-pages --force
                '''
            }
        }
    }
}
