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
                powershell """ Write-Host 'Helloworld'
                ${src}='sometjig'
                Write-Host ${src}
                ${src}
                """ 
            }
        }
    }
}
