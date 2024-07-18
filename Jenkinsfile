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
    options{ /// using option we can specify the time that pipeline should execute 
    //(with in the time it get complets)
        timeout(time: 2, unit: 'SECONDS')
        disableConcurrentBuilds()
       
    }
    environment{
        Greetings = "Good Morning"  // environments are like variables....key value pairs

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
            stage('apply'){
                steps{

                sh 'echo This is from apply'
                }

            }

            stage('destroy'){
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
}


