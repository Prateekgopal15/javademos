pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World!!!"'
        sh '''mvn -f javademos/javademos-master/pom.xml -B -DskipTests clean package
'''
      }
    }

  }
}