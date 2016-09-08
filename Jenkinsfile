#!groovy

node('node') {


    currentBuild.result = "SUCCESS"

    try {

       stage 'Checkout'


       stage 'Test'


       stage 'Build Docker'


       stage 'Deploy'


       stage 'Cleanup'


        }


    catch (err) {

    }

}
