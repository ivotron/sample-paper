pipeline {
  stages {
    stage('popper check') {
      steps {
        checkout scm
        echo 'Popper check started'
        def result = sh "docker run --rm -v `pwd`:`pwd` -v /usr/bin/docker:/usr/bin/docker -v /var/run/docker.sock:/var/run/docker.sock --workdir `pwd` ivotron/popperci-experimenter"
        echo 'Popper check finished'
        echo 'status: ${result}'
      }
    }
  }
}
