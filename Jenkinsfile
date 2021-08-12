pipeline{
  agent any
  stages{
    stage("scm checkout"){
      steps{
            git credentialsId: 'github-cred-id', url: 'https://github.com/DEVOPS2021PTP/java-maven-sample-war.git'
           }
          }
     stage("Maven Build"){
       steps{
            sh "mvn clean package"
            }
        }
       stage("deploy on tomcat"){
       steps{
          sshagent(['demo-deploy-cred']) {
          sh 'scp -o StrictHostKeyChecking=no target/Example-0.0.1-SNAPSHOT.war ec2-user@172.31.14.242:/opt/apache-tomcat-9.0.52/webapps/' 
            }
          }
        }
      }
    }	
