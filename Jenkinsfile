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
        stage("Run game.py") {
            steps {
                sh """
                    python game.py
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
