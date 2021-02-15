pipeline{
    agent{ node{ label 'master' }}
    options{
        buildDiscarder(logRotator(numToKeepStr: '2'))
        disableConcurrentBuilds()
        disableResume()
        timestamps()
        parallelsAlwaysFailFast()
    }
    stages{
        stage('stage1'){
            steps{
                echo "In stage1"
                sh 'sleep 2'
            }
        }
        stage('stage2'){
            parallel{
                stage('stage2-p1'){
                    steps{
                        echo "In parallel-1 for stage2"
                        sh 'sleep 2'
                    }
                }
                stage('stage2-p2'){
                    steps{
                        echo "In parallel-2 for stage2"
                        sh 'sleep 2'
                    }
                }
            }
        }
    }
}
