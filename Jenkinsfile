pipeline {
  agent {
    docker {
      image 'docker:20.10-dind'
      args '--privileged -v /var/lib/docker'
    }
  }
  stages {
    stage('Build') {
      steps {
        sh 'docker version'
        sh 'docker build -t myapp .'
      }
    }
  }
}
