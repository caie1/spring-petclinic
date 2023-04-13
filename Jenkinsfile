#!/usr/bin/env groovy
properties([pipelineTriggers([githubPush()])])

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'cd /var/lib/jenkins/.jenkins/workspace/emma_pipeline && ./mvnw package'
            }
        }

        stage('Run') {
            steps {
                sh 'cd /var/lib/jenkins/.jenkins/workspace/emma_pipeline && java -jar target/*.jar'
            }
        }
    }
}

