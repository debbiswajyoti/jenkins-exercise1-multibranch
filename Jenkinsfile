pipeline{
    agent{ node{ label 'master' }}
    options{
        buildDiscarder(logRotator(numToKeepStr: '2'))
        disableConcurrentBuilds()
        disableResume()
        timestamps()
    }
    stages{
        stage('stage1'){
            steps{
                echo "In stage1"
                sh 'sleep 2'
            }
        }
        stage('stage2'){
            steps{
                echo "In stage2"
                sh 'sleep 2'
            }
        }
    }
}
