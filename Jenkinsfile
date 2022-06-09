node {  
    def mvnhome = tool name: 'mvn-home', type: 'maven' 
    stage('Git-Checkout') { 
        git branch: 'main', credentialsId: 'git-cred', url: 'https://github.com/Cmisenga/web-app2.git'
    }
    stage('Clean-Compile') { 
        sh "${mvnhome}/bin/mvn clean compile" 
    }
    stage('Package') { 
        sh "${mvnhome}/bin/mvn package"
    }
}
