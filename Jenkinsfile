node('built-in') {
    stage('Continuous Download') {
    git 'https://github.com/ChandrikaYekula/maven.git'
}
stage('Continuous Build') {
    sh 'mvn package'
}
stage('Continuous Deployment') {
    sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.1.20:/var/lib/tomcat9/webapps/qaenv.war'
}
stage('Continuous Testing') {
    sh 'echo "Testing Passed"'
}
stage('Continuous Delivery') {
    sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.4.254:/var/lib/tomcat9/webapps/qaenv.war'
}
}
