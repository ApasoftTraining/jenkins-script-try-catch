node {
    stage('Start') {
        echo 'Starting the pipeline...'
    }

    stage('Build') {
        try {
            echo 'Starting the build process...'
           
            sh 'exit 1'  // This simulates an error
            echo 'Build completed successfully!'
        } catch (Exception e) {
            echo "Build failed: ${e.getMessage()}"
            // Here you can take actions in case of failure, such as notifying a team or cleaning up resources.
            currentBuild.result = 'FAILURE'
        }
    }
  
    stage('End') {
        if (currentBuild.result == 'FAILURE') {
            echo 'Pipeline finished with errors.'
        } else {
            echo 'Pipeline completed successfully!'
        }
    }
}
