properties([pipelineTriggers([pollSCM('* * * * *')])])

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Upgrade helm chert"
                sh "helm upgrade -i webapp ./"
                echo 'Done'
            }
        }
    }
}
