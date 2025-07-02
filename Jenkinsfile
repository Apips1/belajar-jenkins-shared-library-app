@Library("belajar-jenkins-shared-library@main") _

import programmerzamannow.jenkins.Output;

node {
    stage('Hello World') {
        hello.world()
    }
}
node {
    stage('Hello Groovys') {
        Output.hello(this, 'Groovy')
    }
}

node {
    stage('Gobal Variable') {
        echo(author())
        echo(author.name())
        echo(author.channel())
    }
}