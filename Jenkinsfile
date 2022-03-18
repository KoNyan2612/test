pipeline {
  agent any
  tools {
      maven 'Maven 3.8.2'
      jdk 'Jdk9'
  }
  stages {
    stage ('set up') {
      steps {
        echo "hello world"
      }
    }
    stage ('build') {
      steps {
        echo "building"
      }
    }
    stage ('test') {
      steps {
        echo 'testing tools installation'
        sh '''
            mvn -v
            java -version
            javac -version
        '''
        nodejs ('Nodejs 16.10') {
            sh '''
                node -v
                npm -v
            '''
        }
      }
    }
  }
}
