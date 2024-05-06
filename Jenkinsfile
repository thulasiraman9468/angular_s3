pipeline {
    agent any

    stages {
        stage('Check1') {
            steps {
                git branch: 'main', url: 'https://github.com/thulasiraman9468/angular_s3.git'
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
                // sh 'ng build'
            }
        }
        stage('Deploy') {
            steps {
                sh 'aws s3 cp  --recursive ./dist/app/browser/ s3://rama-vina-050520241/'
            }
        }
    }
}