pipeline {
    agent {
        node {
            label 'PHP-CSF-STAGING'
        }
    }
    stages { 
        stage('Example') {
            steps {
                echo 'Hello World'
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
}
