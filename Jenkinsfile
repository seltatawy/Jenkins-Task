pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
              
              echo '>>> Start Build'
              sh 'mvn clean install'
               echo '>>> Build Successsssssssssssssssss'
               }
                   }
        stage('Test') { 
            steps {
              
              echo '>>> Start Testinggggggggggggg'
              sh 'mvn test'
               echo '>>> Test Successsssssssssssssssss'
               }
                   }
        
        stage('Deploy') { 
            steps {
              
              echo '>>> Start Deployment'
             sh 'cd /var/lib/jenkins/workspace/Pipeline-Test01/target/'
             sh 'cp *.jar /tmp'
               echo '>>> Deployment Successsssssssssssssssss'
               }
                   }
    }
}
