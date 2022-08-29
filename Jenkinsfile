pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                git url: "https://github.com/Nagireddypalanki/vCard.git"
            }   
        }
        stage("execute Ansible") {
           steps {
                ansiblePlaybook credentialsId: 'root', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'hosts', playbook: 'nginx-playbook.yaml'
            }    
        }    
    }
}
