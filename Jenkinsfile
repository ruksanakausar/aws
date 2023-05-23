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
    stage('SSH1'){
  sshPut remote: remote, from: 'ruksana_24.sh', into: '/home/opc'
 }
  stage('SSH2'){
     sshCommand remote: remote, command: "sudo sh /home/opc/ruksana_24.sh"
    } 
   stage('SSH3'){
 sshCommand remote: remote, command: "pwd"
 }
  stage('SSH4'){
 sshRemove remote: remote, path: "rm -rf /home/opc/ruksana_24.sh"
 }
}
