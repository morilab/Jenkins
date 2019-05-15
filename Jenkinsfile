// ----------------------------
// Declarative Pipeline記法 
// ----------------------------
pipeline {
  agent {
    // ジョブ実行先
    label 'docker'
  }
  stages {
    stage('SCM') {
      steps {
        sh 'pwd'
        sh 'ls -laF'
      }
    }
  }
}
