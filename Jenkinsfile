  pipeline {
  agent any
  
    tools{
      maven 'Maven 3.6.0'
    }
    stages {
    stage("Create Docker Container") {
      steps {
        echo "building container..."
      }
    }
    stage("Test maven") {
      steps {
          sh '''
            echo "Java_Home = $(java -version)"
            echo "Maven_Home = $(mvn -version)"
          '''
      }
    }
      stage("Deploying sAPI") {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
        steps {
<<<<<<< HEAD
          sh 'mvn -f sapi/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
=======
 				  sh 'mvn -f sapi/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
>>>>>>> ac5c5cc08e40bb38b0f7b19cfad3bb38c5af45ee
      }
    }
      stage("Deploying pAPI") {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
        steps {
<<<<<<< HEAD
          sh 'mvn -f papi/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
=======
 				  sh 'mvn -f papi/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
>>>>>>> ac5c5cc08e40bb38b0f7b19cfad3bb38c5af45ee
      }
    }
      stage("Deploying eAPI") {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
        steps {
<<<<<<< HEAD
          sh 'mvn -f eapi/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
=======
 				  sh 'mvn -f eapi/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
>>>>>>> ac5c5cc08e40bb38b0f7b19cfad3bb38c5af45ee
      }
    }
    stage("Finishing Task") {
      steps {
        echo "Deployment Completed on CH..."
      }
    }
  }
}