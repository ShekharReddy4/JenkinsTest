pipeline {
    
    agent any
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
                powershell """ Write-Host ${pwd}.Path
                $src='sometjig'
                Write-Host $src
                $src
                """ 
            }
        }
    }
}
