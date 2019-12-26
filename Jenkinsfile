pipeline {
    agent any
    stages {
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
     

           }
       }
