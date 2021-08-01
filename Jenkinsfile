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
               // sh 'cd /jarfile'
	        sh 'rm -rfv /jarfile/*'
                sh 'cd /var/lib/jenkins/workspace/Pipeline-Test01/target/'
                sh 'cp *.jar /jarfile'
             //sh 'find ./ -name "*.jar" -print0 | xargs -0 cp -t /jarfile/'
               // sh 'Jar-file-name=${find ./ -name "*.jar" -print0}'
            // echo '/jar/*.jar'
                echo 'file moved to "/jarfile/*.jar"'
            
               echo '>>> Deployment Successsssssssssssssssss'
               }
                   }
    }
}
