pipeline {
    agent any
    stages {
<<<<<<< HEAD
        stage ('Checking out'){
             steps {
                     git credentialsId: '49136400-f47b-4ede-a0c9-0f45cc2feb29', url: 'https://github.com/Kamalsankhla/angular-dotnet.git', branch: 'master'

                   }
                  }
           
=======
                stage ('Sonarqube'){
                       environment {
                                 scannerHome = tool 'SonarQubeScanner'
                               }
                       steps {
                                  withSonarQubeEnv('sonarqube'){
                                         sh(script: "sonar-scanner", returnStdout: true)
                                      }
                                  timeout(time: 10, unit: 'MINUTES') {
                                          waitForQualityGate abortPipeline: true
                                      }
                               }
                             }
     
>>>>>>> b6ad649bed6371564b9eccac52ac6c50ea2eebfe

           }
       }
