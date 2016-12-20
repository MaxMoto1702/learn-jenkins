#!groovy

node {
    stage {
        checkout([
                $class                           : 'GitSCM',
                branches                         : [
                        [name: '*/master']
                ],
                doGenerateSubmoduleConfigurations: false,
                extensions                       : [],
                submoduleCfg                     : [],
                userRemoteConfigs                : [
                        [url: 'https://github.com/MaxMoto1702/learn-jenkins.git']
                ]
        ])
    }
    stage('Build') {
        sh './gradlew build'
    }
    stage('Test') {
        sh './gradlew test'
    }
    stage('Deploy') {
        sh './gradlew war'
    }
}
