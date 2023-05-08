pipeline{
    agent {
        label "dev-agent"
    }
    stages{
        //git down
        stage('Prepare'){
             agent {
               label "dev-agent"
            }

           steps{
                echo "pwd"
                
                git url: "https://github.com/yunho1210/cicdtest.git",
                    branch: "main",
                    credentialsId: "git-token-for-jenkins"

            }
        }
    }
}
//tests
//test2