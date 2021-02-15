pipeline{
    agent{ node{ label 'master' }}
    options{
        buildDiscarder(logRotator(numToKeepStr: '2'))
        disableConcurrentBuilds()
        disableResume()
        timestamps()
    }
    stages{
        stage('stage-11'){
            steps{
                echo "In stage1"
                sh 'sleep 3'
            }
        }
        stage('stage-2'){
            steps{
                echo "In stage2"
                sh 'sleep 3'
            }
        }
	stage('stage-3'){
	    steps{
		echo "In stage3"
		sh 'sleep 3'
	    }
	}   
    }
}
