pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: We run testing tool like pytest here'

                # Add permision
                chmod +x /home/ecamposa/Lab6/mlip/bin/activate

                # Activate virtual environment
                source /home/ecamposa/Lab6/mlip/bin/activate

                # Run pytest inside the virtual environment
                pytest .

                # Deactivate virtual environment
                deactivate

                echo 'Testing is done'
                '''

            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our porject'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
