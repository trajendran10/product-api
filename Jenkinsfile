pipeline {

  agent any
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }
    stage('Test') {
      steps {
          bat "mvn test"
      }
    }
    stage('Deployment') {
      steps {
            bat 'mvn -U -V -e -B -DskipTests -Pdev deploy -DmuleDeploy -s "C:\\ProgramData\\Jenkins\\.m2\\settings.xml"'
      }
    }
  }
}