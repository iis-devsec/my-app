
node {
 stage('SCM Checkout'){
	 
	git 'https://github.com/iis-devsec/my-app'
   
   }
   
   stage('Compile-Package & Source-code Analysis'){
	def mvnHome = tool name: 'maven 3.6.3', type: 'maven'    
           withSonarQubeEnv('sonjen2') { 
	   sh "${mvnHome}/bin/mvn package sonar:sonar"
	 }
      
   }
}
/*
   stage('SonarQube Analysis') {
        def mvnHome =  tool name: 'maven 3.6.3', type: 'maven' 
        withSonarQubeEnv('sonarjen') { 
          sh "${mvnHome}/bin/mvn sonar:sonar"
        }
    }
    
    */

