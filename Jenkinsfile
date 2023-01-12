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
                echo 'Deployin......'
		
            }
        }
    }
}
