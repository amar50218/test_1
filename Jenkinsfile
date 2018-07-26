pipeline {
  agent any
  stages {
    stage('gitcheckout') {
      steps {
        git(url: 'https://github.com/amar50218/project.git', branch: 'master', credentialsId: 'bc97a384-77db-4a06-8f9a-0d0754390d89', poll: true)
      }
    }
    stage('gitpush') {
      steps {
        bat(script: 'D:\\code\\file.bat', encoding: 'git push', returnStatus: true, returnStdout: true)
      }
    }
  }
}