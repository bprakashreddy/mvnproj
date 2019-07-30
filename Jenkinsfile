node{
   stage('SCM Checkout') {
   git 'https://github.com/bprakashreddy/mvnproj.git'
   }
   stage('compile-package') {
   def mvnhome= tool name: 'mvn3.5', type: 'maven'
   sh "${mvnhome}/bin/mvn package"
  }
}
