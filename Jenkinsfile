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
                powershell '''
                Write-Host 'helloworld'
                "$src='C:\\Users\\Administrator\\Desktop'"
                "Write-Host $src"
                '''
            }
        }
    }
}
