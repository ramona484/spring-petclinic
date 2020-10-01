pipeline {
   agent none
   stages {     
    stage('Maven Install') {
      agent {         
       docker {          
         image 'maven:3.5.0'         
     }       
    stages {
        stage ('Checkout'){
            steps{
            git 'https://github.com/Ramona84/spring-petclinic'
        }
    }
    stage('Build'){
        steps {
            sh 'mvn clean package'
            junit '**/target/surefire-reports/TEST-*.xml'
        }
    }
    }
}