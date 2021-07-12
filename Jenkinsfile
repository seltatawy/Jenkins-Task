pipeline {
    agent any 
    stages {
        stage('SCM Checkout') { 
            steps {
                
              echo '>>> Start getting SCM code'
              git 'https://github.com/seltatawy/Jenkins-Task.git'
              echo '>>> End getting SCM code'
            }
        }
        stage('Build') { 
            steps {
                // 
                echo 'Build completed'
            }
        }
        stage('Test') { 
            steps {
                // 
                echo 'Test Completed'
            }
        }
        stage('Deploy') { 
            steps {
                // 
                echo 'Deployment completed'
            }
        }
    }
}
