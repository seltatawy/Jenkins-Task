pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
              // sh "mvn clean verify" 
              echo '>>> Start Build'
               sh 'mvn -Dmaven.test.failure.ignore=true install'
               echo '>>> Build Success'
                //junit 'target/surefire-reports/**/*.xml'
            }
        }
        
    }
}
