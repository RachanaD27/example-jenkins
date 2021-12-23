pipeline {
     agent any
         stages {
                 stage('Deploy to Cloudhub') { 
                  
                   steps {
                            bat 'mvn clean deploy -DmuleDeploy -DskipTests -Dmule.version=%version% -Danypoint.username=%username% -Danypoint.password=%password% -Denv=%env% -Dappname=%appname% -Dbusiness=%business% -DvCore=%vCore% -Dworkers=%workers% -Dproperties=%env%'
                         }
                    }
         }
     }
     
     
