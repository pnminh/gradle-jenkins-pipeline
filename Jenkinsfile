node {
    // Clean workspace before doing anything
    deleteDir()
    // Mark the code checkout 'stage'....
      stage ('Stage Checkout'){

            // Checkout code from repository and update any submodules
            checkout scm
       }
      stage ('Print environment variables'){
        //branch name from Jenkins environment variables
         sh "printenv"
        }
}