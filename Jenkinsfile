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
        // Only run if Maven wrapper exists
        if (fileExists('mvnw.cmd') || fileExists('mvnw')) {
            maven('clean compile')
        } else {
            echo "No Maven wrapper found. Make sure your project has mvnw.cmd"
            error("Maven wrapper not found")
        }
    }
}
