pipeline {
    agent any

    triggers { 
        pollSCM('* * * * *')
    }
    parameters { choice(name: 'CHOICES', choices: ['validate', 'clean', 'package'], description: 'my choices') }
    
    
        stages {
            stage('update and install'){
                steps{
                    sh "sudo apt update"
                    sh "sudo apt install openjdk-17-jdk maven -y"
                }
            }
            
                stage('gitclone'){
                    steps{
                        git url: "https://github.com/Ajjuguttuvinay-rs/spring-petclinic.git", branch: 'main'
                    }
                }
                stage('build'){
                    steps{
                        sh "$CHOICES"
                    }
                }
            }
}
        


    

