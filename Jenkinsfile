pipeline {
 agent any
  stages {
   stage ('Build') {
    steps {
          //commands rlated to building the code
		 //  sh "mvn clean install" 
		 // skipping this stage as Jenkins is crashing
	        echo " SInce you asked"
		  
		  }
 
    }
   stage('deploy ') { 
    steps {
        // COmmands related to code deployment
		// copy the war file to tomcat server
	  sshagent(['root']) {
          sh "scp -o StrictHostKeyCHecking=no target/SimpleTomcatWebApp.war  root@43.204.22.29:/home/ec2-user/tomcat/apache-tomcat-10.1.18/webapps"
		 }
		  }
    }
   stage('test') {
    steps {
     // commands related to testing
	      echo " This is deploy stage"
		  }
       }
    }
}
