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
                sh """
                 echo 'This is TEST'
                ls -lrt
                
                """
            }
        }
 
        
   }
    post {
        always {
            echo 'i will always say hello agin'
            deleteDir()
        }
    }
}