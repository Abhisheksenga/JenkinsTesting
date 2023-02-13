pipeline {
    agent any
    stages {
        
        stage('Set Parameters') {
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
