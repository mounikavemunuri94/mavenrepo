pipeline{

agent any

triggers{
// poll repo every 2 minute for changes
pollSCM('* * * * *')
}

stages{

stage('git') {

steps{
checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '569ebd4e-dc65-4c07-81f9-8d9973f604c3', url: 'https://github.com/mounikavemunuri94/mavenrepo.git']]])

}
} // stage 1 closed

stage('build'){
steps{
sh 'mvn package '
}
}// stage 2 closed


}// stages closed


}// pipelineclosed
