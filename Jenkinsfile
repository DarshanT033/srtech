pipeline {
    agent any

    stages {
        stage('Clone-Repo') {
	    	steps {
	        	checkout scm
	    	}
        }
	stage('Build') {
		steps {
			sh 'mvn install'
		}
	}	
 	stage('Deployment') {
	   steps {
		sh 'scp target/srtech.war root@172.31.93.248:/root/tomcat/apache-tomcat-10.1.61/webapps'
	}
    }
}
}
