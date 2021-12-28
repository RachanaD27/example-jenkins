pipeline { 
	agent any 	
		stages {
				stage('Build and Deploy to Standalone Server'){

					steps { 
						script{
                            
                           
							def deployenv =params.ENVIRONMENT_TO_DEPLOY
							def versionv = deployenv+'_DEPLOY_MULE_VERSION'
							def targetserverv=deployenv+'_DEPLOY_TARGET_SERVER' 
							def deployusernamev= deployenv+'_DEPLOY_USERNAME'
							def deploypasswordv=deployenv+'_DEPLOY_PASSWORD' 
							def anypointurlv=deployenv+'_DEPLOY_ANYPOINT_URL'
							
							
						    def version = env."${versionv}"
							def targetserver=env."${targetserverv}"
							def deployusername=env."${deployusernamev}" 
							def deploypassword=env."${deploypasswordv}"
							def anypointurl=env."${anypointurlv}"
							

                            bat 'mvn clean deploy -DmuleDeploy -DskipTests -Dmule.version=${version} -Danypoint.username=${username} -Danypoint.password=${password} -Denv=${env} -DvCore=${vCore} -Dworkers=${workers} -Dproperties=${env}'
                         

}
}
}
} 
}
      