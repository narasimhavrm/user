pipeline {
  agent {
    node { label 'workstation'}
  }

  stages {

    stage('Build ') {
          steps {
            sh 'npm install'
          }
    }

    stage('Unit Test ') {
          steps {
            echo 'Unit Test'
//             sh 'npm test'
          }
    }

    stage('Code Analysis ') {
          steps {
            sh 'sonar-scanner -Dsonar.host.url=http://sonarqube:9000 -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectKey=user'
          }
    }

    stage('Security scan ') {
          steps {
            echo 'Security scan'
          }
    }
    
    stage('Publish Artifact ') {
          steps {
            echo 'Publish Artifact'
          }
    }

  }

}