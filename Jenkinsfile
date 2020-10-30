pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World!!!"'
        sh 'mvn -f javademos_master/javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
      }
    }

  }
}