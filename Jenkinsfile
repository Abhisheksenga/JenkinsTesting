pipeline {
   agent { node { label('!Rcdn-Node11') } } 
    stages {
        stage('Set Parameters for selecting branch to build') {
             steps {
                script { 
                    properties([
                        parameters([
                            choice(
                                choices: ['ONE', 'TWO'], 
                                name: 'BRANCH',
                                description: 'Select Branch for build'
                            )])
                        ])
                }
             }
        }
        stage('Selected Branch') {
            steps {
                    sh """
                    echo "deploy to production ${params.BRANCH}"
                    """
                }
            }
   
    }
}
