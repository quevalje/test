pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                git log
            }
        }
    }
}


node {
   env.GIT_COMMIT = sh(script: "git rev-parse HEAD", returnStdout: true).trim()
   env.GIT_PREVIOUS_COMMIT = sh(script: "git rev-parse HEAD^1", returnStdout: true).trim()
   env.RESULT = sh(script: "git diff --name-only $GIT_PREVIOUS_COMMIT $GIT_COMMIT", returnStdout: true).trim()
   echo env.GIT_COMMIT
   echo env.GIT_PREVIOUS_COMMIT
   echo env.RESULT
}