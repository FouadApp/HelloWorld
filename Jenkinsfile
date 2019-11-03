pipeline {
    agent none
    stages {
        stage('Parallel Stages') {
            parallel {
                stage('DEPLOY JAR SERVICE ON SLAVE 1 ') {
                    agent {
                        node {
                            label 'slave1'
                            customWorkspace "${env.WORKSPACE}/${env.JOB_NAME}_${env.BUILD_ID}"
                        }
                    }
                    steps {
                        echo 'your command copy file'
                    }


                }
                stage('DEPLOY JAR ROUTER ON SLAVE 2') {
                    agent {
                        node {
                            label 'slave2'
                            customWorkspace "${env.WORKSPACE}/${env.JOB_NAME}_${env.BUILD_ID}"
                        }
                    }
                    steps {
                        echo 'your command copy file router.jar '
                    }


                }
                stage('DEPLOY JAR FRONT ON SLAVE 3') {
                    agent {
                        node {
                            label 'slave3'
                            customWorkspace "${env.WORKSPACE}/${env.JOB_NAME}_${env.BUILD_ID}"
                        }
                    }
                    steps {
                        echo 'your command copy file front.jar '
                    }


                }

            }


        }
    }



}
