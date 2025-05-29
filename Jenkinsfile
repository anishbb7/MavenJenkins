pipeline{
agent any
tools{
maven 'Maven'
}
stages{
stage('Checkout'){
steps{
git branch: 'master', url: 'https://github.com/anishbb7/MavenJenkins.git'
}
}
stage('Build'){
steps{
sh 'mvn clean package'
}
}
stage('Test'){
steps{
sh 'mvn test'
}
}
stage('Run Application'){
steps{
sh 'java -jar target/MavenJenkins-1.0-SNAPSHOT.jar'
}
}
}
post{
success{
echo 'Success'
}
failure{
echo 'Failed'
}
}
}
