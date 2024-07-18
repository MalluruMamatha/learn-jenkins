// pipeline {
//     agent any
//     options {
//         // Timeout counter starts AFTER agent is allocated
//         timeout(time: 1, unit: 'SECONDS')

//     }
//     stages {
//         stage('Example') {
//             steps {
//                 echo 'Hello World'
//             }
//         }
//     }

//     post { 
//         always { 
//             echo 'I will always say Hello again!'
//         }
// }
// }


pipeline{
    agent {
        label 'AGENT-1'
    }
    options{
        timeout(time: 30, unit: 'MINUTES')
    }
    environment{
        Greetings = "Good Morning"
    }

    parameters{
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    }

    stages{

        stage('init'){
            steps{

                sh 'echo This is from init'

            }
        }
            stage('plan'){
                steps{

                sh 'echo This is from plan'

            }
            }
            stage('iapply'){
                steps{

                sh 'echo This is from apply'
                }

            }
    }

    post{

        always{
            echo 'always say hello' 
        }
        success{
            echo 'i will when pipeline is success'

        }
        failure{
            echo 'i will ren when pipeline is failure'

        }
    }
}


