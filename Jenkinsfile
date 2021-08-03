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
        stage('Deploy_Approval'){
          steps {
              timeout(time: 10, unit: 'MINUTES') {
                input(id: "Deploy or not", message: "Deploy ${params.project_name}?", ok: 'Deploy')
              }
        }
        }
         stage('Deploy') { 
            steps {
              
              echo '>>> Start Deployment'
               sh 'rm -rfv /jarfile/*'
               sh 'cp /var/lib/jenkins/workspace/Pipeline-Test01/target/*.jar /jarfile'
               echo 'file moved to "/jarfile/*.jar"'
            
               echo '>>> Deployment Successsssssssssssssssss'
               }
        } 
     }
}
