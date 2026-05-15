pipeline {
    agent any
    tools {
        jdk "java17"
        maven "maven 12"
    }

    triggers { 
        pollSCM('* * * * *')
    }
    parameters { choice(name: 'CHOICES', choices: ['validate', 'clean', 'package'], description: 'my choices') }
    
    
        stages {
            stage('update'){
                steps{
                    sh "sudo apt update"
                }
            }
            

                stage('build'){
                    steps{
                        echo "Choice: ${params.CHOICES}"
                    }
                }
            }
}
        


    

