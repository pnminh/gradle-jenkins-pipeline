node {
    // Clean workspace before doing anything
    deleteDir()
    // Mark the code checkout 'stage'....
      stage ('Stage Checkout'){

            // Checkout code from repository and update any submodules
            checkout scm
       }
      stage ('Stage Build'){
        //branch name from Jenkins environment variables
         sh "echo 'My branch is: ${env.BRANCH_NAME}'"
        }
}