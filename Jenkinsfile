pipeline {
    agent {label 'master'}
    options {
        timestamps()
        disableConcurrentBuilds()
        buildDiscarder(logRotator(numToKeepStr: '10'))
        timeout(time: 150, unit: 'MINUTES')
    }
    stages {
        stage('PR check') {
            steps {
                    sh '''
                        echo "Trigger a Pull Request"
                        sleep 10s
                       '''
            }
        }
    }
}
