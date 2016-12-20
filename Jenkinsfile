#!groovy

node {
    stage('compile') {
        sh './gradlew compileJava'
    }
    stage('test') {
        sh './gradlew test'
    }
    stage('build') {
        sh './gradlew test'
    }
}
