#!groovy

node {
    stage('chckout') {
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
    stage('ls') {
        sh 'ls -Al'
    }
//    stage('compile') {
//        sh './gradlew compileJava'
//    }
//    stage('test') {
//        sh './gradlew test'
//    }
//    stage('build') {
//        sh './gradlew test'
//    }
}
