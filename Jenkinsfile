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
                powershell 'Write-Output "Hello, World!"'
                powershell "Write-Output 'Hello, World!'"
                powershell """ $src1= 'C:\\Users\\Administrator\\Desktop\\Jenkins\\workspace\\GHPL1'
                $dst1= 'C:\\Users\\Administrator\\Desktop\\site'
                Get-ChildItem $src1 -Filter '*' | Copy-Item -Destination $dst1 -Force """
            }
        }
    }
}
