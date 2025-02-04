pipeline {
    agent any

    stages {
        stage("Run Frontend") {
            steps {
                echo 'Executing yarn...'
                nodejs('Node-10-17') {
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
