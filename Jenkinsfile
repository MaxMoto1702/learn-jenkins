#!groovy

node('node') {


    currentBuild.result = "SUCCESS"

    try {

       stage 'Checkout'

            checkout scm

       stage 'Test'

            env.NODE_ENV = "test"

            print "Environment will be : ${env.NODE_ENV}"


       stage 'Build Docker'

            echo 'Build Docker'

       stage 'Deploy'

            echo 'Push to Repo'

            echo 'ssh to web server and tell it to pull new image'

       stage 'Cleanup'

            echo 'prune and cleanup'

            mail body: 'project build successful',
                        from: 'smv@live.ru',
                        replyTo: 'smv@live.ru',
                        subject: 'project build successful',
                        to: 'maxim.serebryanskiy@icloud.com'

        }


    catch (err) {

        currentBuild.result = "FAILURE"

            mail body: "project build error: ${err}" ,
            from: 'smv@live.ru',
            replyTo: 'smv@live.ru',
            subject: 'project build failed',
            to: 'maxim.serebryanskiy@icloud.com'

        throw err
    }

}
