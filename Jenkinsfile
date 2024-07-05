pipeline {
    agent  {
        label 'Agent1'
    }
    options {
        
        timeout(time: 30, unit: 'MINUTES')
    }

    stages {

        stage('TEST') {
            steps {
                sh 'echo This is TEST'
                ls -lrt
                sh 'sleep 10'
            }
        }
 
        
   }
    post {
        always {
            echo 'i will always say hello agin'
            deletedir()
        }
    }
}