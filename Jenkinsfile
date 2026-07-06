pipeline{
    agent any
    stages{
        stage('1-clone'){
            steps{
                echo "Cloning into repository"
            }
        }
        stage('2-parallel-jobs'){
            parallel{
                stage('1-subjob1'){
                    steps{
                        echo "Running sub-job 1"
                    }   
                }
                stage('2-subjob2'){
                    steps{
                        echo "Running sub-job 2"
                    }
                }
            }
        }
        stage('3-codetest'){
            steps{
                echo "Running code test"
            }
        }
        stage('4-closing'){
            when {
                branch 'feature'
            }
            steps{
                echo "we are done"
            }
        }
    }
}