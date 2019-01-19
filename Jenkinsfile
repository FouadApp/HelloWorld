pipeline {

agent {
  
    label 'slave_1'
    customWorkspace '/Stage/fares/slave_1'
  
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
