pipeline {
    
    agent none
    stages {
        agent {
    label 'Slave1'
    }
        stage('Build') { 
            steps { 
              bat 'dir' 
            }
        }
        stage('Test'){
            agent {
    label 'Slave1'
    }
            steps {
              bat 'ipconfig'
            }
        }
        stage('Deploy') {
            agent {
    label 'Slave1'
    }
            steps {
                powershell '''
                "$src='C:\\Users\\Administrator\\Desktop\\Jenkins\\workspace\\GHPL1'"
                "$dst='C:\\Users\\Administrator\\Desktop\\site'"
                "Get-ChildItem $src -Filter '*' | Copy-Item -Destination $dst -Force"
                '''
            }
        }
    }
}
