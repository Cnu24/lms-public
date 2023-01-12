pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building & Deploy VM'
		sh 'cd webapp && rm -rf dist'
		sh 'cd webapp && npm install'
                sh 'cd webapp && npm run build'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying.......'
                sh 'scp -r webapp/dist ubuntu@172.31.11.255:/var/www/html/
            }
        }
    }
}
