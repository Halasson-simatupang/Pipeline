#!groovy
pipeline {
    agent {
        node {
            label 'PHP-CSF-STAGING'
        }
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    }
    stages { 
        stage('Example') {
            steps {
                echo "Hello World ${params.PERSON}"
            }
        }
        stage('Paralel') {
             parallel {
                stage('Branch A') {
                    steps {
                        echo "On Branch A"
                    }
                }
                stage('Branch B') {
                    steps {
                        echo "On Branch B"
                    }
                }
             }
        }
    }
    post {
        always {
            archiveArtifacts 'Jenkinsfile'
        }
    }
}
