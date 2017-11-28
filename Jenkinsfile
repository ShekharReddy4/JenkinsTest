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
                powershell $(pwd).Path
                powershell '$(vart) = "C:\\Users\\Adminstratot\\Desktop"'
                powershell 'Write-Host "$(vart)"'
                
            }
        }
    }
}
