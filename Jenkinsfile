pipeline {
    agent {
    node {
        label 'Slave1'
    }
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
                powershell 'Write-Output "Hello, World!"'
                powershell "Write-Output 'Hello, World!'"
                powershell "$dst= 'C:\\Users\\Administrator\\Desktop\\site'"
                powershell "$src= $pwd.Drive.CurrentLocation"
                powershell "Get-ChildItem $src -Filter '*' | Copy-Item -Destination $dst -Force"
                
            }
        }
    }
}
