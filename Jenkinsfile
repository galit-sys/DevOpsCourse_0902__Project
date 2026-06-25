properties([pipelineTriggers([pollSCM('* * * * *')])])

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Upgrade helm chert"
                sh "cd Phase_III/webapp/"
                sh "helm upgrade -i webapp ./"
                echo 'Done'
            }
        }
        stage('Test') {
            steps {
                echo "Check pod status"
                sh "cd Phase_III/webapp/"
                sh "kubectl get pod"
                echo 'Done'
            }
        }
        stage('Deploy') {
            steps {
                echo "Create package"
                sh "cd Phase_III/webapp/"
                sh "helm package ./webapp "
                echo 'Done'
            }
        }
    }
}
