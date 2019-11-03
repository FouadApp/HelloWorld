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
                        sh ' echo "your command copy file " '
                    }
                    post {

                        always {
                            echo "-----------------------------------THE END ------------------------------"
                        }


                        failure {
                            echo 'failure:  Error when executing : thank you to consult the logs on Jenkins  '

                        }

                        success {

                            echo '         *********** Build and deploy to nexus  was a success ***************************'

                            deleteDir()
                            echo '   Delete workspace  ${env.JOB_NAME}   was a success'

                        }

                    }

                }
                stage('DEPLOY JAR ROUTER ON SLAVE 2') {
                    agent {
                        node {
                            label 'slave1'
                            customWorkspace "${env.WORKSPACE}/${env.JOB_NAME}_${env.BUILD_ID}"
                        }
                    }
                    steps {
                        sh 'echo " your command copy file router.jar"   '
                    }
                    post {

                        always {
                            echo "-----------------------------------THE END ------------------------------"
                        }


                        failure {
                            echo 'failure:  Error when executing : thank you to consult the logs on Jenkins  '

                        }

                        success {

                            echo '         *********** Build and deploy to nexus  was a success ***************************'

                            deleteDir()
                            echo '   Delete workspace  ${env.JOB_NAME}   was a success'

                        }

                    }

                }

                stage('DEPLOY JAR FRONT ON SLAVE 3') {
                    agent {
                        node {
                            label 'slave2'
                            customWorkspace "${env.WORKSPACE}/${env.JOB_NAME}_${env.BUILD_ID}"
                        }
                    }
                    steps {
                        sh 'echo " your command copy file front.jar"   '
                    }
                    post {

                        always {
                            echo "-----------------------------------THE END ------------------------------"
                        }


                        failure {
                            echo 'failure:  Error when executing : thank you to consult the logs on Jenkins  '

                        }

                        success {

                            echo '         *********** Build and deploy to nexus  was a success ***************************'

                            deleteDir()
                            echo '   Delete workspace  ${env.JOB_NAME}   was a success'

                        }

                    }

                }

            }



        }
    }

}
