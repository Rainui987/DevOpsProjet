node {

stage('SCM'){
 git 'https://github.com/Rainui987/DevOpsProjet/tree/master/microservice-compte-comptable'
}

stage('Compile'){
def mvnHome = tool name: 'maven-3' , type: 'maven'
sh "${mvnHome}/bin/mvn package"
}

stage('SonarQube') {
  def mvnHome = tool name: 'maven-3' , type: 'maven'
  sh "${mvnHome}/bin/mvn sonar:sonar -Dsonar.host.url=http://192.168.1.73:9000"
    }
}
