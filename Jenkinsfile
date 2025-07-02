@Library("belajar-jenkins-shared-library@main") _

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    hello.world()
                }
            }
        }

        stage('Use Class') {
            steps {
                script {
                    import programmerzamannow.jenkins.Output
                    Output.hello(this, 'Groovy Declarative')
                }
            }
        }

        stage('Global Variable') {
            steps {
                echo author()
                echo author.name()
                echo author.channel()
            }
        }

        stage('Maven Build') {
            steps {
                maven('clean compile')
            }
        }
    }
}
