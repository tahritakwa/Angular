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
            stage('Build'){
                steps{
                 script{
                  sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml "
                   }
                  }
              }

  }
  }
