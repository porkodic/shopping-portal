pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
        sleep 4
      }
    }

    stage('test') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
        sleep 4
      }
    }

    stage('package') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
        sleep 4
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}