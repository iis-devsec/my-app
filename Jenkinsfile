
node {
 stage('SCM Checkout'){
	 
	git 'https://github.com/iis-devsec/my-app'
   
   }
	
	  stage('SonarQube analysis') {
    def scannerHome = tool name: 'sonjen2', type: 'hudson.plugins.sonar.SonarRunnerInstallation'
    withSonarQubeEnv('My SonarQube Server') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
/*	
   
   stage('Compile-Package & Source-code Analysis'){
	def mvnHome = tool name: 'maven 3.6.3', type: 'maven'    
           withSonarQubeEnv('sonjen2') { 
	   sh "${mvnHome}/bin/mvn package sonar:sonar"
	 }
      
   }
*/
}
/*
   stage('SonarQube Analysis') {
        def mvnHome =  tool name: 'maven 3.6.3', type: 'maven' 
        withSonarQubeEnv('sonarjen') { 
          sh "${mvnHome}/bin/mvn sonar:sonar"
        }
    }
    
    */

