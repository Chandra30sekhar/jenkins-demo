pipeline{
	agent any
	stages{
    	stage('Build'){
    		steps{
    		    echo "Cloning to the repository..."
			git clone https://github.com/Chandra30sekhar/simple-java-maven-app.git
			
    		}
    	}
    
    	stage('Installing'){
    	    steps{
    		    echo "Installing"
		    mvn package
    	    }
    		}
	stage('Testing'){
		steps{
			echo "Testing"
			mvn test
		}
	}
	stage('Deploying'){
		steps{
			echo "Deploying"
			java -jar /var/lib/jenkins/workspace/git-jenkinsfile-demo/target/my-app-1.0-SNAPSHOT.jar
		}
	}
	}
}

