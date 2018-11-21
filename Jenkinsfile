
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
    stage("Test MVN") {
      steps {
 				  sh '''
            echo "Java_Home = $(java -version)"
            echo "Maven_Home = $(mvn -version)"
          '''
      }
    }
      stage("Compile sAPI") {
      steps {
 				  sh 'mvn -f /sapi/pom.xml compile'
      }
    }
    stage("Finishing Task") {
      steps {
        echo "Deployment Completed on CH..."
      }
    }
  }
}
