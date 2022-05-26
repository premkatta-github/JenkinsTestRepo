// pipeline {
//     agent any

//     stages {
//         stage('Hello') {
//             steps {
//                 echo 'Gradle clean started !!'
//                 sh '/usr/local/bin npm -v'
//                 sh 'cd /Users/premkatta/.jenkins/workspace/PipeLine_Github_JenkinsRepo/android/ && ./gradlew clean'
//                 echo 'Build stared !!'
//                 sh './gradlew assembleRelease'
//                 echo 'Build Completed !!'
//                 sh 'cd /Users/premkatta/Documents && mkdir JenkinsBuilds && cd JenkinsBuilds && mkdir android'
//                 sh 'cd /Users/premkatta/.jenkins/workspace/PipeLine_Github_JenkinsRepo/android/'
//                 sh 'mv app/build/outputs/apk/release/app-universal.apk /Users/premkatta/Documents/JenkinsBuilds/android/'
//                 echo 'apk moved to Documents/JenkinsBuilds/android'
//             }
//         }
//     }
// }


pipeline {
    agent any
    stages {
        stage('android') {
            steps {
                echo 'Gradle clean started !!'
                sh '/usr/local/bin/node -v'
                sh 'export PATH=$PATH:/usr/local/bin ; cd /Users/premkatta/.jenkins/workspace/PipeLine_Github_JenkinsRepo/ ; /usr/local/bin/npm i ; cd android ; ./gradlew clean ; ./gradlew assembleRelease'
            }
        }
    }
}

