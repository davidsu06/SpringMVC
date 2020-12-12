pipeline {
  agent any

  stages {
    stage('Package') {
        steps {
            powershell label:'', script:"""
                mvn package -DskipTests=true
            """
        }
    }
    
    stage('Deploy') {
        steps {
            powershell label:'', script:"""
                cd target/
                copy HelloWorld.war C:/Users/juanj/Documents/apache-tomcat-9.0.41/webapps
            """
        }
    }
  }
}
