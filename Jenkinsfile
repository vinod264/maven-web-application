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

}

//Execute the sonarQube Report
stage('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}

//Upload Artifacts into Artifactory Repo
stage('UploadArtifactsintoNexus'){
sh "${mavenHome}/bin/mvn deploy"
}

