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
                "$src='C:\\Users\\Administrator\\Desktop\\Jenkins\\workspace\\GHPL2'"
                "$dst='C:\\Users\\Administrator\\Desktop\\site2'"
                "Get-ChildItem $src -Filter '*' | Copy-Item -Destination $dst -Force"
                '''
            }
        }
    }
}
