pipeline{
agent any

tools{
maven 'Maven'
}

stages{
stage('Checkout'){
steps{
git branch:'master',url:'https://github.com/sowjanya2004/Maven.git'
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

stage('Run applictaion'){
steps{
sh 'java -jar target/MavenJenkins-1.0-SNAPSHOT.jar'
}
}
}
}

post{
success{
echo 'success build'
}
failure{
echo 'build failure'
}
}
