
 pipeline{
 agent any
 stages{

 stage('code checkout'){
  steps{
   git branch: 'main', credentialsId: 'toper', url: 'https://github.com/edigagangadhar99/jenkins-ansible.git
       }
 }

 stage('Execute Ansible'){
  steps{   
      ansiblePlaybook credentialsId: 'pass', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml'
      }
 }
    }

}
