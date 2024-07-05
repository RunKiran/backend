pipeline {
    agent  {
        label 'Agent1'
    }
    options {
        
        timeout(time: 30, unit: 'MINUTES')
    }

    stages {

        stage('Install dependencies') {
            steps {
                sh """
                  npm install
                
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