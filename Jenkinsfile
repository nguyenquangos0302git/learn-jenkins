pipeline {
  agent any
  stages {
    stage("Clean up") {
      steps {
        deleteDir()
      }
    }
    stage("Clone Repo") {
      steps {
        sh "git clone https://github.com/jglick/simple-maven-project-with-tests.git"
      }
    }
    stage("Build") {
      steps {
        dir("simple-maven-project-with-tests") {
          sh "mvn clean install"
        }
      }
    }
    // stage("Test") {
    //   steps {
    //     dir("simple-maven-project-with-tests") {
    //       sh "mvn test"
    //     }
    //   }
    // }
  }
}