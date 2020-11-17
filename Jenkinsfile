pipeline {
agent any
stages {
stage("scm") {
steps {git 'https://github.com/Rajkamal996/demo.git'}
}
stage ("build") {
steps {
bat 'mvn clean'
bat 'mvn install'
}
}
stage ("Deploy") {
steps {bat 'xcopy /y "C:\\Windows\\System32\\config\\systemprofile\\AppData\\Local\\Jenkins\\.jenkins\\workspace\\adam\\target\\my-app.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"'}
}
}
}

