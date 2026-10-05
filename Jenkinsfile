node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
	    sh 'rm /var/jenkins_home/workspace/BuildSampleApp/tempdir'
            sh 'docker stop samplerunning'
            sh 'docker rm samplerunning'
        }
    }
    stage('Build') {
        build 'BuildSampleApp'
    }
    stage('Results') {
        build 'TestSampleApp'
    }
}
