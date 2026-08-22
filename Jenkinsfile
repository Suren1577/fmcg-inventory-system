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

        stage('SonarQube Analysis') {
            steps {
                // 'SonarQube' must match the exact server name you configured in Jenkins System Settings
                withSonarQubeEnv('SonarQube') {
                    sh 'mvn sonar:sonar'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying branch: ${env.BRANCH_NAME}"
            }
        }
    }
}