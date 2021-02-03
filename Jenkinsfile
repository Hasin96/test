
 
pipeline {
    /* specify nodes for executing */
    agent {
        label any
    }
    triggers {
        githubPush()
    }
 
    stages {
        /* checkout repo */
        stage('Checkout SCM') {
            steps {
                checkout([
                 $class: 'GitSCM',
                 branches: [[name: 'main']],
                 userRemoteConfigs: [[
                    url: 'git@github.com:Hasin96/test.git',
                    credentialsId: '',
                 ]]
                ])
            }
        }
         stage('Do the deployment') {
            steps {
                echo ">> Run deploy afpplications "
            }
        }
    }
 
    
}
