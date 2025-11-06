pipeline {
    agent any

    tools {
    maven 'Maven' 
  configuration  
}
stages {
    stage ('checkout') {
        steps {
            git branch: 'main' , url : 'https://github.com/gayu1606/java-ci-sample-git'
            //  {
                
            }
        }

    }
    stage ('Build') {
        steps {
            sh 'mvn clean install'
        }
}
stage ('Test') {
    steps {
        sh 'mvn test'
    }
}
}
post {
    always {
        junit '**/target/surefire-reports/*.xml
        }
        
    }
}

