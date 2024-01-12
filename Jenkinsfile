pipeline {
    agent {
        node {
            label 'Gerrit-10.10.101.1'
        }
    }
	// 此步废弃，直接Jenkins agent方式执行
    environment {
        REMOTE_PASSWORD = credentials('10.10.101.1')
    }

    stages {
        stage('Execute Script') {
            steps {
                script {
                    sh """
					 sudo -u devops bash -c 'python /devops/sit214_new/leigao6/GerritMain.py $GroupName $ProjectName '
                    """
                }
            }
        }
    }
}
