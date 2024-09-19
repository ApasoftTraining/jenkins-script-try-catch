node {
    stage('Start') {
        echo 'Starting the pipeline...'
    }

   stage('Try-catch'){
        try {
           //block
           echo 'Starting the test'
           sh 'exit 1'
           echo 'Test succesful'
        } catch (Exception e) {
            //commands
            echo "Test failed ${e.getMessage()}"
            currentBuild.result ='FAILURE'
        }
    }

    stage('End'){
        if (currentBuild.result=='FAILURE'){
            echo 'Pipeline finished with errors'
        }
        else {
            echo 'Pipeline finished successfully'
        }
    }
}
  
    
