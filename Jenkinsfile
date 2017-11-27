pipeline {
    
    agent {
        label 'Slave1'
    } 
    stages {
        stage('Build') { 
            steps { 
              bat 'dir' 
            }
        }
        stage('Test'){
            steps {
              bat 'ipconfig'
            }
        }
        stage('Deploy') {
            steps {
                bat 'xcopy C:\\Users\\Administrator\\Desktop\\Jenkins\\workspace\\GHPL1\\: C:\\Users\\Administrator\\Desktop\\site\\: /s /e'
            }
        }
    }
}
