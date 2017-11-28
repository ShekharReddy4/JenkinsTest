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
                "$src='C:\\Users\\Administrator\\Desktop\\Jenkins\\workspace\\GHPL1'"
                "$dst='C:\\Users\\Administrator\\Desktop\\site'"
                "Get-ChildItem $src -Filter '*' | Copy-Item -Destination $dst -Force"
                
                '''
            }
        }
    }
}
