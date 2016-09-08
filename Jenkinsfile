#!groovy

node('node') {

    currentBuild.result = "SUCCESS"

    try {
        stage 'Clean'
        print "Start cleaning..."
        sh './gradlew clean'
        print "Finish cleaning."

        stage 'Test'
        print "Start testing..."
        sh './gradlew test'
        print "Finish testing."

        stage 'Build'
        print "Start building..."
        sh './gradlew build'
        print "Finish building."

        mail body: 'project build successful',
                from: 'smv@live.ru',
                replyTo: 'smv@live.ru',
                subject: 'project build successful',
                to: 'maxim.serebryanskiy@icloud.com'
    }

    catch (err) {

        currentBuild.result = "FAILURE"

        mail body: "project build error: ${err}",
                from: 'smv@live.ru',
                replyTo: 'smv@live.ru',
                subject: 'project build failed',
                to: 'maxim.serebryanskiy@icloud.com'

        throw err
    }
}
