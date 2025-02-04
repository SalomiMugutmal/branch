pipeline {
    agent any

    stages {
        stage("Run Frontend") {
            steps {
                echo 'Executing yarn...'
                nodejs('NodeJS23.7.0') {
                    bat 'yarn install'  // ✅ Use `bat` instead of `sh`
                }
            }
        }
        
        stage("Run Backend") {
            steps {
                echo 'Executing Gradle...'
                withGradle {
                    bat 'gradlew.bat -v'  // ✅ Use `gradlew.bat` instead of `./gradlew -v`
                }
            }
        }
    }
}
