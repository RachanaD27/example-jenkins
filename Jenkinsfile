pipeline {
     agent any
         stages {
             stage('Build') {
                 steps {
                     
                     bat 'mvn clean install'
                     }
                 }
             stage('Test') {
                 steps {
                     
                     bat 'mvn test'
                       }
                 }
                 stage('Deploy to Cloudhub') { 
                  
                   steps {
                            bat 'mvn clean deploy -DmuleDeploy -DskipTests -Dmule.version=4.3.0 -Danypoint.username=RachanaD4 -Danypoint.password=Ra8147825331 -Denv=Sandbox -Dappname=example-jenkins1 -Dbusiness=nous_infosystems -DvCore=Micro -Dworkers=1 -Dproperties=dev'
                         }
                    }
         }
     }