pipeline{
    agent any
    parameters{
        string(name:'BRANCH_NAME', defaultvalue:'main', description:'Git branch to build')
        booleanparam(name:'RUN_TESTS', defaultvalue:'true', description:'Runtest')
        choice(name:'ENV', choices:['dev', 'stage','test'], description:'Select environment')
    }
    stages{
        stage('Info'){
            steps{
                echo "Branch :${params.BRANCH_NAME}"
                 echo "RUN TESTS :${paramS.RUN_TESTS}"
                  echo "ENV :${params.ENV}"
            }
        }
    }
}
