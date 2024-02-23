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

                # TODO fill out the path to conda here
                # sudo /home/yiwenz5/miniconda3/etc/profile.d/conda.sh init
                source /home/yiwenz5/miniconda3/etc/profile.d/conda.sh
                conda activate mlip
                pytest
                conda deactivate
                # modify code
                # TODO Complete the command to run pytest
                # sudo /home/yiwenz5/miniconda3/etc/profile.d/conda.sh run -n mlip pytest
                # test
                # echo 'pytest not runned'
                # exit 1 #comment this line after implementing Jenkinsfile
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