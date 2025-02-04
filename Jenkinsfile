pipeline {
    agent any

    stages {
        stage("Run Frontend") {
            steps {
                echo 'Executing yarn...'
                nodejs(version: 'NodeJS23.7.0') {
                    sh 'yarn install'
                }
            }
        }
        
        stage("Run Backend") {
            steps {
                echo 'Executing Gradle...'
                withGradle {
                    sh './gradlew -v'
                }
            }
        }
    }
}
