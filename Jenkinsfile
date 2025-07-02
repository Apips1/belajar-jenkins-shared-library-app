@Library("belajar-jenkins-shared-library@main") _
import programmerzamannow.jenkins.Output

node {
    stage('Hello World') {
        hello.world()
    }

    stage('Hello Groovy') {
        Output.hello(this, 'Groovy')
    }

    stage('Global Variable') {
        echo author()
        echo author.name()
        echo author.channel()
    }
     stage('Debug Maven') {
        // Debug information
        echo "Current directory: ${pwd()}"
        if (isUnix()) {
            sh 'ls -la'
            sh 'ls -la .mvn/ || echo "No .mvn directory"'
        } else {
            bat 'dir'
            bat 'dir .mvn\\ || echo "No .mvn directory"'
        }
    }

    stage('Maven Build') {
        maven('clean compile')
    }
}
