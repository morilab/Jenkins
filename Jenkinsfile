// ----------------------------
<<<<<<< HEAD
// Declarative Pipeline記法
// ----------------------------
pipeline {
  //---------------------------
  // エージェント
  //---------------------------
  agent {
    // ジョブ実行先を絞る場合に記載
    label 'docker'
  }
  
  //---------------------------
  // ビルドトリガ
  //---------------------------
  triggers {
    pollSCM('*/1 9-23 * * 1-5') // SCMポーリング周期(1分毎、9:00〜23:00、月〜金)
  }
  
  //---------------------------
  // 変数定義
  //---------------------------
  environment {
    BRANCH = 'master'
  }
  
  //---------------------------
  // ビルドトリガ
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
// Declarative Pipeline險俶ｳ� 
// ----------------------------
pipeline {
  agent {
    // 繧ｸ繝ｧ繝門ｮ溯｡悟��
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
