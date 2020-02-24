pipeline {
    agent any
   pipeline {
    agent any	
    stages {
        stage('Non-Parallel Stage') {
            steps {
                echo 'This stage will be executed first.'
            }
        }
        stage('Parallel Stage') {
            failFast true
            parallel {
                stage('并行环节1') {
                    steps {
                        echo "并行一"
                    }
                }
                stage('并行环节2') {
                    steps {
                        echo "并行二"
                    }
                }
                stage('并行环节3') {
                    stages {
                        stage('Nested 1') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                            }
                        }
                        stage('Nested 2') {
                            steps {
                                echo "In stage Nested 2 within Branch C"
                            }
                        }
                    }
                }
            }
        }
    }
  }
}
