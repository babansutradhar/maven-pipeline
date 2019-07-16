
node{
	stage('SCM Checkout'){
	  git 'https://github.com/babansutradhar/maven-pipeline'
	 }
	 stage('Compile-Packages'){
	 // Get maven home path
	 def mvnHome = tool name: 'maven3', type: 'maven'
	 sh "${mvnHome}/bin/mvn package"
	 }
	 stage('Email Notification'){
	   mail bcc: '', body: '''Hi welcome to jenkins email alarts
	   Thanks
	   Baban''', cc: '', from: '', replyTo: '', subject: 'Jenkins job', to: 'baban.unified@gmail.com'
	 }
	}