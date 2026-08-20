pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building FMCG Inventory System'
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing FMCG Inventory System'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying branch: ${env.BRANCH_NAME}"
            }
        }
    }
}
