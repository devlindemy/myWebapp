pipeline {
    agent any
	
	  tools{
       maven 'MAVEN_HOME'
    }
 stages {
      stage('checkout') {
           steps {
             
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/devlindemy/myWebapp.git']])
             
          }
        }
	 stage('Build') {
           steps {
                sh 'mvn package'             
          }
        }


}
}
