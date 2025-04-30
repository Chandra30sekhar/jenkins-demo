pipeline{
	agent any

	tools{
		maven "maven"
	}
	
	stages{
    	stage('Build'){
    		steps{
    		sh "rm -d -f simple-java-maven-app"
		sh "git clone https://github.com/Chandra30sekhar/simple-java-maven-app.git"
			
    		}
    	}
    
    	stage('Installing'){
    	    steps{
    		    
		    sh "mvn package"
    	    }
    		}
	stage('Testing'){
		steps{
			
			sh "mvn test"
		}
	}
	stage('Deploying'){
		steps{
			
			sh "java -jar /var/lib/jenkins/workspace/git-jenkinsfile-demo/target/my-app-1.0-SNAPSHOT.jar"
		}
	}
	}
}

