pipeline {
    agent {
        node {
            label 'my-defined-label'
            customWorkspace "/var/www/html/jenkins12345"
        }
    }
    stages {
        stage("foo") {
            steps {
                echo "Workspace dir is ${pwd()}"
            }
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
