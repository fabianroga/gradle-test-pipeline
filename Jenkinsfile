#!/usr/bin/env groovy
properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '5')), pipelineTriggers([GenericTrigger(causeString: 'Generic Cause', regexpFilterExpression: '', regexpFilterText: '', token: 'gradle-test-pipeline', tokenCredentialId: '')])])
node {
    stage('checkout'){
        checkout scmGit(branches: [[name: "${env.BRANCH_NAME}"]], extensions: [], userRemoteConfigs: [[credentialsId: 'git_credentials', url: 'https://github.com/fabianroga/gradle-test-pipeline.git']])
    }
    echo "Hello, World"
    stage('Build') {
        echo "Build Gradle App"
    }
    sh "ls"
}
