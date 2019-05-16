pipeline {
    agent {
        label 'docker'
    }
    
    stages {
        stage('docker-build') {
            steps {
                sh 'docker build -t acu-m0:lint .'
            }
        }
        stage('lint') {
            environment {
                PID = powershell(
                    returnStdout: true,
                    script: 'docker run -itd acu-m0:lint /bin/sh'
                ).trim()
            }
            steps {
                sh 'docker exec $PID csh lint.sh'
                sh 'docker cp ${PID}:/home/genetec/vlog_lint.xml vlog_lint.xml'
                junit 'vlog_lint.xml'
            }
        }
        stage('compile') {
            steps {
                echo "Compile"
            }
        }
    }
}