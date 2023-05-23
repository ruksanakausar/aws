node{
  def remote = [:]
  remote.name = 'oraclevm'
  remote.host = '152.67.160.182'
  remote.user = 'opc'
  remote.password = 'Muzammil073#'
  remote.allowAnyHosts = true
  stage('checkout') {
    checkout scm
  }
    stage('step1'){
  sshPut remote: remote, from: 'ruksana_24.sh', into: '/home/opc'
 }
  stage('step2'){
     sshCommand remote: remote, command: "sudo sh /home/opc/ruksana_24.sh"
    } 
   stage('step3'){
 sshCommand remote: remote, command: "pwd"
 }
  stage('step4'){
 sshRemove remote: remote, path: "/home/opc/ruksana_24.sh"
 }
}
