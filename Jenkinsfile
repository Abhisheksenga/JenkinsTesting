pipeline {
    agent any
    parameters {

        choice(name: 'BRANCH', choices: ['master', 'release'], description: 'Select a branch')

    }
    stages {
        stage('Example') {
            steps {
                echo "Branch selected: ${params.BRANCH}"

            }
        }
    }
}
