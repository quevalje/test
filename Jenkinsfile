pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
                echo $GIT_PREVIOUS_COMMIT
                echo $GIT_COMMIT
            }
        }
    }
}