pipeline {
   agent {
        node {
            label 'AGENT-1'
       }
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
                echo 'deploy'
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