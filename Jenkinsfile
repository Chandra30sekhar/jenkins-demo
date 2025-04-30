pipeline{
	agent any
	stages{
    	stage('Build'){
    		steps{
    		
		git clone https://github.com/Chandra30sekhar/simple-java-maven-app.git
			
    		}
    	}
    
    	stage('Installing'){
    	    steps{
    		    
		    mvn package
    	    }
    		}
	stage('Testing'){
		steps{
			
			mvn test
		}
	}
	stage('Deploying'){
		steps{
			
			java -jar /var/lib/jenkins/workspace/git-jenkinsfile-demo/target/my-app-1.0-SNAPSHOT.jar
		}
	}
	}
}

