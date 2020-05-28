pipeline {
    agent {
        node {
            customWorkspace "/var/www/html/jenkins12345/${JOB_NAME}_${BUILD_NUMBER}"
        }
    }
    post {
        cleanup {
            /* clean up our workspace */
            deleteDir()
            /* clean up tmp directory */
            dir("${workspace}@tmp") {
                deleteDir()
            }
            /* clean up script directory */
            dir("${workspace}@script") {
                deleteDir()
            }
        }
    }
}