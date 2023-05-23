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
    sshput remote:remote, from: 'ruksana_24.sh',into:'/home/opc'
  }
  stage('step2'){
    sshccommand remote:remote, command: "sudo sh /home/opc/ruksana_24.sh"
  }
  stage('step2'){
    sshcommand remote:remote,command:"pwd"
  }
  stage('step3'){
    sshcommand remote:remote,command:"mv/home/opc/ruksana_24.sh /home/opc/ruksana_24"/
      }
}
