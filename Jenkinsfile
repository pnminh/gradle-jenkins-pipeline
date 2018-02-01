node {
    // Clean workspace before doing anything
    deleteDir()
    // Mark the code checkout 'stage'....
    stage('Stage Checkout') {

        // Checkout code from repository and update any submodules
        checkout scm
    }
    stage('Print environment variables') {
        //branch name from Jenkins environment variables
        sh "printenv"
    }
    stage('Get branch name') {
        //this will check the current branch (with *), and only keep the branch name (omit * and space)
        GIT_BRANCH = sh(
                script: 'git branch | grep \\* | cut -d \' \' -f2',
                returnStdout: true
        ).trim()
        sh "echo $GIT_BRANCH"
    }
    stage ('release'){
        sh "./gradlew clean build release"
    }
}