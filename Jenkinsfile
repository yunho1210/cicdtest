pipeline{
    agent any

    triggers{
        pollSCM('* * * * *')
    }

    stages{
        //git down
        stage('Prepare'){
            agent any

            steps{
                echo "clonning repository"


                git url: 'https://github.com/yunho1210/cicdtest.git',
                    branch: 'main',
                    credentialsID: 'token for jenkins , git test'
            }
            post{
                success{
                    echo "pull success"
                }

                always{
                    echo "i tried..."
                }

                cleanup{
                    echo "all end "
                }
            }
        }
    }
}