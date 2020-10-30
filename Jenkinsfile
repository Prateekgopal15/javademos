pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World!!!"'
        sh 'mvn -f javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**/target/*.war', fingerprint: true)
        sh '''echo "mkdir /source/buildoutput/${BUILD_NUMBER}"

mkdir /source/buildoutput/${BUILD_NUMBER}

echo "cp **/target/*.war /source/buildoutput/${BUILD_NUMBER}"

cp /var/lib/jenkins/workspace/javademos_master/javademos-master/ssgsems/target/*.war /source/buildoutput/${BUILD_NUMBER}

echo "Done!!!"'''
      }
    }

  }
}