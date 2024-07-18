pipeline {
    agent any
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 1, unit: 'SECONDS')

    }
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
        }
}
}