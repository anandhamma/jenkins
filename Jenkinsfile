pipeline {
    agent {
        label "windows"
    }
    tools {
        maven 'Maven3.5.4'
  
    }
    node ('master') {
        stage 'checkout' {
            checkout scm
            }
        }

        stage 'Build' {
            steps {
                    bat 'cd NumberGenerator'
            }
             post {
                success {
                    junit 'NumberGenerator/target/surefire-reports/*.xml'
                        }
                 }
               

           
            }
        }
    

