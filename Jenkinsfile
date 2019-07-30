node{
   stage('SCM Checkout') {
   git 'https://github.com/bprakashreddy/mvnproj.git'
   }
   stage('compile-package') {
   def mvnhome= tool name: 'mvn3.5', type: 'maven'
   sh "${mvnhome}/bin/mvn package"
  }
   stage('Slack notification') {
   slackSend baseUrl: 'https://hooks.slack.com/services/',
   channel: '#jenkins-pipeline-demo', 
   color: 'good', iconEmoji: '', 
   message: 'welcome to jenkins, slack!',
   teamDomain: 'javahomecloud', 
   tokenCredentialId: 'slack-demo', username: ''
  }
}
