pipeline{
	agent{
		label 'slave-machine-1'
	}
	stages{
		stage('1-Code-Check'){
			steps{
				sh 'lsblk'
			}
		}
		stage('2-parallel-jobs'){
			parallel{
				stage('sub-job1'){
					steps{
						sh 'free -h'
					}
				}
				stage('lscpu'){
					steps{
						sh 'free -g'
					}
				}
			}
		}
		stage('3-Repo-clone'){
			agent{
				label 'slave-machine-2'
			}
			steps{
				sh 'logname'
			}
		}
	}
}