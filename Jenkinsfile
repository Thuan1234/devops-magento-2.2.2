pipeline {
    agent {
        node {
            label 'g1test'
            customWorkspace "/var/www/html/g1/customWorkSpace"
        }
    }
    stages {
        stage("foo") {
            steps {
                echo "Workspace dir is ${pwd()}"
            }
        }
    }
}
