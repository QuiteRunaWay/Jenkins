pipeline {
    agent any

    stages {
        stage('Git') {
            steps { git branch: 'main', credentialsId: '403df8ec-8909-411c-8c68-112ad597cbe1', url: 'git@github.com:QuiteRunaWay/Jjenkins.git' }
                }
        stage('Molecule') {
            steps { sh 'molecule test' }
                          }
            }
        }
