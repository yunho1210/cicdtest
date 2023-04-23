pipeline{
    agent any

    trigger{
        pollSCM('* * * * *')
    }

    stages{
        //git down
        stage('Prepare'){
            agent any

            steps{
                echo "clonning repository"


                gir url: 'https://github.com/yunho1210/cicdtest.git',
                    branch: 'main',
                    credentialsID: 'token for jenkins , git test'
            }
            post{
                success{
                    echo "pull 성공"
                }

                always{
                    echo "i tried..."
                }

                cleanup{
                    echo "사후처리 전부 끝"
                }
            }
        }
    }
}