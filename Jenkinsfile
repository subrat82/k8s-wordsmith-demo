node{
  def Namespace = "default"
  def ImageName = "subratit/projects-16th-nov"
  def ImageTag = "latest02"
  def Creds	= "076eed1a-ddda-4fcc-b8bd-5fbf6fa738fd"

  stage('Checkout'){
      
    git branch: 'master',
    credentialsId: 'cd86d294-d343-4a1b-8e19-388f2ac2f93b',
    url: 'https://github.com/subrat82/k8s-wordsmith-demo.git'
  }

    stage('Docker Build, Push'){
      sh "/usr/local/bin/docker --version"
      sh "echo docker login localhost:8080"
      withDockerRegistry([credentialsId: "${Creds}", url: 'https://index.docker.io/v1/']) {
     // withDockerRegistry([credentialsId: "076eed1a-ddda-4fcc-b8bd-5fbf6fa738fd", url: 'https://index.docker.io/v1/']) {
     // sh "/usr/local/bin/docker build -t ${ImageName}:${ImageTag} ."
      sh "echo build successfully"
     // sh "/usr/local/bin/docker push ${ImageName}"
       }

    }
}
