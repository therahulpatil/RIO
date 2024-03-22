pipeline {
   agent any 
   tools {
        maven 'Maven3.6.3' 
    }
   
   stages {
       stage('SCM CheckOut'){
          steps {
            git 'https://github.com/therahulpatil/RIO'
          }
          }
      stage('Compile-Package'){
         steps {
             sh "mvn -version" 
             sh "mvn package"
              }
         }
   }
   post {
      always {
         cleanWs()
      }
   }
}
