pipeline { 
	agent any 	
		stages {
				stage('Build and Deploy to Standalone Server'){

					steps { 
						script{
                            
                            def deployenv =params.env
                           // def branch = params.Branch
							
							def versionv = deployenv+'_DEPLOY_MULE_VERSION'
							def targetserverv=deployenv+'_DEPLOY_TARGET_SERVER' 
							def deployusernamev= deployenv+'_DEPLOY_USERNAME'
							def deploypasswordv=deployenv+'_DEPLOY_PASSWORD' 
							def deployvCorev=deployenv+'_DEPLOY_VCORE'
				            def deployworkersv=deployenv+'_DEPLOY_WORKERS'
				            def deploypropertiesv=deployenv+'_DEPLOY_ENV'
													
						   			
                            def version = env."${versionv}"
							def targetserver=env."${targetserverv}"
							def deployusername=env."${deployusernamev}" 
							def deploypassword=env."${deploypasswordv}"
							def deployvCore=env."${deployvCorev}"
							def deployworkers=env."${deployworkersv}"
							def deployproperties=env."${deployenv}"
							

                            bat 'mvn clean deploy -DmuleDeploy -DskipTests -Dmule.version=${version} -Danypoint.username=${username} -Danypoint.password=${password} -Denv=${env} -DvCore=${vCore} -Dworkers=${workers} -Dproperties=${env}'
                         

}
}
}
} 
}
      