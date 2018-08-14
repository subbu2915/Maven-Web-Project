#!groovy

node {
	   
	stage('Checkouting'){

          //checkout scm
		git branch: 'stage', credentialsId: '6b7eae3b-30d7-41ad-b367-a9cf9610e492', url: 'https://github.com/subbu2915/Maven-Web-Project.git'

       }

       stage('BuildArtifact'){

          sh 'mvn install'
       }
	   
      //stage('Sonar') {
                    //add stage sonar
                    //sh 'mvn sonar:sonar'
                //}
       
}
