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
        post {  
         always {  
             echo 'This will always run'  
         }  
         success {  
             echo 'This will run only if successful'  
         }  
         failure {  
             mail bcc: '', body: "<b>Example</b><br>Project: ${env.JOB_NAME} <br>Build Number: ${env.BUILD_NUMBER} <br> URL de build: ${env.BUILD_URL}", cc: '', charset: 'UTF-8', from: '', mimeType: 'text/html', replyTo: '', subject: "ERROR CI: Project name -> ${env.JOB_NAME}", to: "foo@foomail.com";  
         }  
         unstable {  
             echo 'This will run only if the run was marked as unstable'  
         }  
         changed {  
             echo 'This will run only if the state of the Pipeline has changed'  
             echo 'For example, if the Pipeline was previously failing but is now successful'  
         }  
     }  
    }
}
