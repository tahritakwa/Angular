pipeline
{
          agent any
           stages {
             stage('Pull') {
              steps{
               script{
                 checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                  userRemoteConfigs: [[
                   credentialsId:'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',
                     url:'https://github.com/tahritakwa/Angular.git']]])
          }
       }
      }
            stage('docker'){
                steps{
                 script{
                  sh "ansible-playbook Ansible/docker.yml -i Ansible/inventory/host.yml "
                   }
                  }
              }

  }
  }
