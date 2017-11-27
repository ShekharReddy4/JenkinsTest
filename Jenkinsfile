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
              powershell "$src12='C:\\Users\\Administrator\\Desktop\\Jenkins\\workspace\\GHPL1'"
                powershell "$src12"
            }
        }
        stage('Deploy') {
            steps {
                powershell 'Write-Output "Hello, World!"'
                powershell "Write-Output 'Hello, World!'"
                powershell """ $src1= 'C:\Users\Administrator\Desktop\Jenkins\workspace\GHPL1'
                $dst1= 'C:\Users\Administrator\Desktop\site'
                Get-ChildItem 'C:\Users\Administrator\Desktop\Jenkins\' -Filter '*' | Copy-Item -Destination $dst1 -Force """
            }
        }
    }
}
