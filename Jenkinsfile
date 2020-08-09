pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'This is the build job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'This is the test job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'This is the package job'
        sh 'npm run package'
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}