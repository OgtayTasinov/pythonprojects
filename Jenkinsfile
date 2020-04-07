pipeline {
    agent any
    stages {
        stage("Create important files") {
            steps {
                sh """
                    touch importanfile1
                    touch importantfile2
                    touch importantfile3                
                """
            } // steps
        }
        stage("Run helloworld") {
            steps {
                sh """
                      python helloworld.py
                """
            } //steps
        } // stage
        stage("Run conditionals.py") {
            steps {
                sh """
                    python conditionals.py
                """
            } //steps
        }  // stage
    } // stages 
    post {
        always {
            sh """
                rm-rf importantfile1
                rm-rf importantfile2
                rm-rf importantfile3
            """
        }
    }  
} //pipeline
