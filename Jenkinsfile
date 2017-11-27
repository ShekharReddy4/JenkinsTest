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
                powershell "$src= 'C:\\Users\\Administrator\\Desktop\\Jenkins\\workspace\\GHPL1'"
                powershell "$dst= 'C:\\Users\\Administrator\\Desktop\\site'"
                
                powershell "Get-ChildItem $src -Filter '*' | Copy-Item -Destination $dst -Force"
                
            }
        }
    }
}
