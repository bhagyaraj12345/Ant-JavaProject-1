#!groovy
node{
 stage('Source'){
     git credentialsId: '165e8383-9d20-4fe9-94f2-7840bc763c7a', url: 'https://github.com/bhagyaraj12345/Ant-JavaProject-1.git'
   
  \* if (env.BRANCH_NAME == 'master') {
  stage 'Only on master'
  println 'This happens only on master branch'
} else {
  stage 'Other branches'
  println "Current branch ${env.BRANCH_NAME}"
} */
 }
 
 stage('Build'){
    /* bat "ant -f build-mt.xml" */ /*For windows machines*/
    sh "ant -f build-mt.xml" 
 }
 stage('Send Email'){
     mail bcc: 'mithunreddytechnologies@gmail.com', body: 'Buils is done', cc: '', from: '', replyTo: '', subject: 'Build Status', to: 'devopstrainingblr@gmail.com'
 }
 /*stage('Archive'){
  archiveArtifacts '/Users/bhaskarreddyl/.jenkins/workspace/Pipeline-Project-Ant-Web/dist/SampleAntProject.war'
 }*/
}

