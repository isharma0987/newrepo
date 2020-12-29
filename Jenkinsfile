pipeline {
    agent any
    
    tools {
         gradle 'gradle'
    }
    stages {
        stage("run frontend") {
            steps {
                echo 'executing yarn....'
                nodejs('node-10.17'){
                    sh 'npm install'
                }
            }
        }
        stage("run backend") {
            steps {
                 echo 'executing gradle....'
                     sh './gradlew -v'
                 }
            }
        }
    }
}
