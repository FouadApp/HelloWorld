pipeline {

agent {

    label any
  
  
}


stages {
         stage("Prepare"){
       steps{
         sh '''
           sh ./test_jenkins.sh
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
