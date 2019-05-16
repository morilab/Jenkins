// ----------------------------
<<<<<<< HEAD
// Declarative Pipeline‹L–@
// ----------------------------
pipeline {
  //---------------------------
  // ƒG[ƒWƒFƒ“ƒg
  //---------------------------
  agent {
    // ƒWƒ‡ƒuŽÀsæ‚ði‚éê‡‚É‹LÚ
    label 'docker'
  }
  
  //---------------------------
  // ƒrƒ‹ƒhƒgƒŠƒK
  //---------------------------
  triggers {
    pollSCM('*/1 9-23 * * 1-5') // SCMƒ|[ƒŠƒ“ƒOŽüŠú(1•ª–ˆA9:00`23:00AŒŽ`‹à)
  }
  
  //---------------------------
  // •Ï”’è‹`
  //---------------------------
  environment {
    BRANCH = 'master'
  }
  
  //---------------------------
  // ƒrƒ‹ƒhƒgƒŠƒK
  //---------------------------
  stages {
    stage('Git CheckOut') {
      steps {
        git url: 'https://github.com/morilab/Jenkins_covered_plugin.git'
        sh 'ls -laF'
      }
    }
    stage('Mercurial CheckOut') {
      steps {
        checkout scm: [
                $class:'MercurialSCM',
                source:'http://dmori@5f-netbsd/kallithea/project/NFT/ACU_M0/ACU_M0_verification',
                clean:false,
                credentialsId:''
            ],
            poll: true
=======
// Declarative Pipelineè¨˜æ³• 
// ----------------------------
pipeline {
  agent {
    // ã‚¸ãƒ§ãƒ–å®Ÿè¡Œå…ˆ
    label 'docker'
  }
  stages {
    stage('SCM') {
      steps {
        sh 'pwd'
>>>>>>> 83191a669ebdfe548b5b32c95ff3201ee9207d5e
        sh 'ls -laF'
      }
    }
  }
}
