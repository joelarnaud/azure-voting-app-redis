pipeline {
   agent any

   stages {
      stage('verify branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Docker Build') {
         steps {
            sh label: '', script: 'docker image ls -a'
            sh label: '', script: 'cd azure-vote; docker image ls -a; docker build -t jenkins-pipeline .; docker image ls -a; cd ..'
         }
      }
   }
}