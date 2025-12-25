pipeline {
  agent any
  stages {
    stage('Fetch Code') {
      steps {
        git(url: 'https://github.com/VikasAIngle/sample-jenkins-repo.git', branch: 'master', poll: true)
      }
    }

    stage('Install Apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy Application') {
      steps {
        sh 'sudo cp -R * /var/www/html'
      }
    }

  }
}