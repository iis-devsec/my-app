
node {
 stage('SCM Checkout'){
	 
	git 'https://github.com/iis-devsec/my-app'
   
   }
   
   stage('Compile-Package'){
	def mvnHome = tool name: 'maven 3.6.3', type: 'maven'    

	   sh "${mvnHome}/bin/mvn package"
	 }
      
   }
   



