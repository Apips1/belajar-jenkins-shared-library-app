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

    stage('Maven Build') {
        maven('clean compile')
    }
}
