pipeline {
  agent any
  stages {
    stage('gitcheckout') {
      parallel {
        stage('gitcheckout') {
          steps {
            git(url: 'https://github.com/amar50218/test_1.git', branch: 'master', credentialsId: 'bc97a384-77db-4a06-8f9a-0d0754390d89', poll: true, changelog: true)
          }
        }
        stage('SCM') {
          steps {
            svn(url: 'https://10.9.17.128/svn/E-06063-01-01/E-06063-01-01/Main/Code/test', changelog: true, poll: true)
          }
        }
        stage('SCM1') {
          steps {
            svn(url: 'file:///D:/Panasonic/svn_test/set', changelog: true, poll: true)
          }
        }
      }
    }
    stage('sleep') {
      parallel {
        stage('sleep') {
          steps {
            sleep(unit: 'MINUTES', time: 2)
          }
        }
        stage('suces') {
          steps {
            bat(script: 'command executed', returnStatus: true, returnStdout: true)
          }
        }
      }
    }
  }
}