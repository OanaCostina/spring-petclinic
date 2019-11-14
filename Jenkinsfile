pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                withMaven(maven: 'maven_installation', mavenSettingsConfig: 'mavensettingsxml') {
                    bat 'mvn -DskipTests clean package'
                }
            }
        }
    }
}
