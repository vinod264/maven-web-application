node{
def mavenHome = tool name: 'maven3.8.5'
//Get the code from Github Repo
stage('CheckoutCode'){
git branch: 'development', credentialsId: 'da17bc5a-141d-4f1e-a709-b311ad6513ff', url: 'https://github.com/vinod264/maven-web-application.git'
}
//Do the build by using Maven Build tool
stage('Build'){
sh "${mavenHome}/bin/mvn clean package"
}
/*


//Execute the sonarQube Report
stage('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}

//Upload Artifacts into Artifactory Repo
stage('UploadArtifactsintoNexus'){
sh "${mavenHome}/bin/mvn deploy"
}

//Deploy Application into Tomcat Server
stage('DeployApplicationTomcatServer'){
sshagent(['6f8d8b07-9861-4bcf-990a-3528e0226771']) {
  sh "scp -o StrictHostkeyChecking=no target/maven-web-application.war ec2-user@13.233.0.92:/opt/apache-tomcat-9.0.62/webapps"
}

}
*/
  
} 
  
