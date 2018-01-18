#!groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''echo "PATH = %PATH%"
       				   echo "MAVEN_HOME = %MAVEN_HOME%"
        		        mvn install''''
            }
        }
        stage('Test') {
            steps {
                bat '''echo "PATH = %PATH%"
       				   echo "MAVEN_HOME = %MAVEN_HOME%"
        		        mvn test''''
            }
        }
        stage('package') {
            steps {
                 bat '''echo "PATH = %PATH%"
       				   echo "MAVEN_HOME = %MAVEN_HOME%"
        		        mvn install'''''
            }
        }
        stage('deploy') {
            steps {
                  
        cd target 
        copy CounterWebApp.war "c:\\apache\\tomcat\\webapps"
        echo "copied successfully"
        '''''
            }
        }
    }
}