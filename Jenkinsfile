pipeline{
agent any
tools{
maven 'Maven'
}
stages{
stage('Checkout'){
steps{
git branch:'main',url:'https://github.com/ankitjha100/mvnselp.git'
}}
stage('Build'){
steps{
sh 'mvn clean package'
}}
stage('Test'){
steps{
sh 'mvn test'
}}
stage('Run'){
steps{
sh 'mvn clean install '
}}}
post{
success{
echo 'Open SauceDemo: https://www.saucedemo.com'
}
failure{
echo 'Build failed'
}}}
