pipeline {
    agent any
    parameters {
        string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Git branch to build')
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run test')
        choice(name: 'ENV', choices: ['dev', 'stage', 'test'], description: 'Select environment')
    }
    stages {
        stage('Info') {
            steps {
                echo "Branch: ${params.BRANCH_NAME}"
                echo "RUN TESTS: ${params.RUN_TESTS}"
                echo "ENV: ${params.ENV}"
            }
        }
        stage('scanes'){
            parallel{
            stage('sonar'){
                steps{
                    echo "sonar is executing"
                    sleep 10
                }
            }stage('docker'){
                steps{
                    echo "docker is executing"
                    sleep 10 
                }
            }stage('amazon'){
                steps{
                    echo "amazon is launching"
                    sleep 10
                }
            }
            }
        }
   }
}
