pipeline
{
agent any
stages
{
stage('build')
{
steps{
sh'npm install'
}
}
stage('deploy')
{
steps{
script{
withEnv(['JENKINS_NODE_COOKIE=dontkill']){
echo 'hi world'
sh 'nohup npm run start:dev&'
}
}
}
}
}
