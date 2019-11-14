pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                withMaven(maven: 'maven_installation', mavenSettingsConfig: 'mavensettingsxml.xml') {
                    bat 'mvn -DskipTests clean package'
                }
            }
        }
    }
}
