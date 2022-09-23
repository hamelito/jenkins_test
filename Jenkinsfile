pipeline {
    agent any 
    stages {
        
        
        stage('Clone') { 
            steps {
            sh "mkdir -p /tmp/master/"    
            sh "rm -rf /tmp/master/*"    
            sh "cd /tmp/master/ && git clone https://github.com/hamelito/jenkins_test.git  "
            }
        }
        
        
        stage('Build') { 
            steps {
            sh "cd /tmp/master/jenkins_test/ && javac Main.java"
            }
        }
        
        
        stage('Run') { 
            steps {
            sh "cd /tmp/master/jenkins_test/ && java Main"
            }
        }
    }
}
