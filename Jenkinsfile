stage('Build') {
  node {
    checkout scm
    sh "npm install"
    stash includes: 'node_modules/', name: 'node_modules'
  }
}

stage('Test') {
  node {
    unstash 'node_modules'
    sh "ls -lrt"
  }
}
