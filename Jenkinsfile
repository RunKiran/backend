pipeline {
    agent  {
        label 'Agent1'
    }
    options {
        
        timeout(time: 30, unit: 'MINUTES')
    }
    environment {
        def appversion = '' //variable declaration
    }

    stages {
        stage (read_versions){
            steps {
                script {
                    def packagejson = readCSV file: 'dir/input.csv'
                    appversion = packagejson.version
                    echo "application version is $appversion"
                }
            }
        }

        stage('Install dependencies') {
            steps {
                sh """
                  npm install
                  ls -lrt
                  echo $appversion
                  echo "application version is $appversion"
                
                """
            }
        stage('Build') {
            steps {
                sh """
                zip -r backend-${appversion}.zip */ -x Jenkinsfile -x backend-${appversion}.zip

                """

            }

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