node{
   stage('SCM Checkout') {
   git 'https://github.com/bprakashreddy/mvnproj.git'
   }
   stage('compile-package') {
   def mvnhome= tool name: 'mvn3.5', type: 'maven'
   sh "${mvnhome}/bin/mvn package"
  }
   stage('Email notifications') {
      mail bcc: '', body: '''Hi, welcome
      thanks
      prakash''', cc: '', from: '', replyTo: '', subject: 'jenkinsfile job', to: 'bprakash1856@gmail.com'
 }
}
