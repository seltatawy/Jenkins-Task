pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
              // sh "mvn clean verify" 
              echo '>>> Start Build'
              // sh 'mvn -Dmaven.test.failure.ignore=true install'
                sh 'mvn clean install'
               echo '>>> Build Successsssssssssssssssss'
                //junit 'target/surefire-reports/**/*.xml'
            }
        }
        
    }
}
