pipeline {
  agent any
  stages {
    stage('popper check') {
      steps {
        echo 'Popper check started'
        sh 'docker run --rm -v `pwd`:`pwd` -v /usr/bin/docker:/usr/bin/docker -v /var/run/docker.sock:/var/run/docker.sock --workdir `pwd` ivotron/popperci-experimenter'
        echo 'Popper check finished'
        sh 'echo "status: $(cat popper_status)"'
      }
    }
  }
}
