
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
        
    

