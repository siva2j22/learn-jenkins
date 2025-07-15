pipeline {
   agent {
        node {
            label 'AGENT-1'
       }
}
        environment {
            GREETING = 'Hello Jenkins'
        }
        options {
            timeout(time: 1, unit: 'HOURS')
            disableConcurrentBuilds()
        }

    // build
    stages {
        stage('Build') {
            steps {
                echo 'building'
            }
        }
        stage('Test') {
            steps {
                echo 'testing'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    echo "i write shell script"
                    echo "$GREETING"
                    sleep 10
                """
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'if pipeline fails used generally fails'
        }
        success { 
            echo 'the stages are success!'
        }
    }
}