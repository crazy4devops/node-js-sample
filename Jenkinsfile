stage('Build') {
  node {
    checkout scm
    sh "npm install"
    stash includes: 'node_modules/', name: 'node_modules'
    sh "ls -lrt "
  }
}

stage('Test') {
  node {
    sh "mkdir -p test"
    dir("./test") {
      unstash "node_modules"
    }
    sh "ls -lrt ./test/*"
  }
}
