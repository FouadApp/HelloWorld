pipeline {

agent  {
  
    label ''
   // customWorkspace '/Stage/fares/slave_1'
  
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
