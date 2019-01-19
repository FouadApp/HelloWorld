pipeline {
agent any
stages {
         stage("Prepare"){
       steps{
         sh '''
           test_jenkins.sh
           '''
         }
     }

     stage ("Build"){
       steps {
         sh '''
           echo "Building app"
         '''
       }
     }
}


}
