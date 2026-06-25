properties([pipelineTriggers([pollSCM('* * * * *')])])

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                sh "ls -ltr"
                echo 'Main Project'
            }
        }
    }
}
