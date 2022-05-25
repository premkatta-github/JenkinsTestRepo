pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Gradle clean started !!'
                sh 'cd /Users/premkatta/.jenkins/workspace/PipeLine_Github_JenkinsRepo/android/ && ./gradle clean'
                echo 'Build stared !!'
                sh './gradle assembleRelease'
                echo 'Build Completed !!'
                sh 'cd /Users/premkatta/Documents && mkdir JenkinsBuilds && cd JenkinsBuilds && mkdir android'
                sh 'cd /Users/premkatta/.jenkins/workspace/PipeLine_Github_JenkinsRepo/android/'
                sh 'mv app/build/outputs/apk/release/app-universal.apk /Users/premkatta/Documents/JenkinsBuilds/android/'
                echo 'apk moved to Documents/JenkinsBuilds/android'
            }
        }
    }
}