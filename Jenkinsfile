// ----------------------------
<<<<<<< HEAD
// Declarative Pipeline�L�@
// ----------------------------
pipeline {
  //---------------------------
  // �G�[�W�F���g
  //---------------------------
  agent {
    // �W���u���s����i��ꍇ�ɋL��
    label 'docker'
  }
  
  //---------------------------
  // �r���h�g���K
  //---------------------------
  triggers {
    pollSCM('*/1 9-23 * * 1-5') // SCM�|�[�����O����(1�����A9:00�`23:00�A���`��)
  }
  
  //---------------------------
  // �ϐ���`
  //---------------------------
  environment {
    BRANCH = 'master'
  }
  
  //---------------------------
  // �r���h�g���K
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
>>>>>>> 83191a669ebdfe548b5b32c95ff3201ee9207d5e
        sh 'ls -laF'
      }
    }
  }
}
