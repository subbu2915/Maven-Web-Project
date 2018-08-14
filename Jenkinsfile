#!groovy

node {
	   
	stage('Checkouting'){

          //checkout scm
		git branch: 'stage', credentialsId: '6b7eae3b-30d7-41ad-b367-a9cf9610e492', url: 'https://github.com/subbu2915/Maven-Web-Project.git'

       }

       stage('BuildArtifact'){

          sh 'mvn install'
       }
	   
	stage('deploy to tomcat'){
		sshagent(['Tomcat']) {
    		sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@172.31.35.113:/opt/apache-tomcat-8.0.53/webapps'
			// some block
}

	}
      //stage('Sonar') {
                    //add stage sonar
                    //sh 'mvn sonar:sonar'
                //}
       
}
