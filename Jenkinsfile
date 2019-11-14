pipeline {
    agent any
    environment {
        MAVEN_INSTALLATION = 'maven_installation'
        MAVEN_SETTINGS_CONFIG = 'mavensettingsxml'
    }
    stages {
        stage('Build') {
            steps {
                withMaven(maven: MAVEN_INSTALLATION, mavenSettingsConfig: MAVEN_SETTINGS_CONFIG) {
                    bat 'mvn -DskipTests clean package'
                }
            }
        }
        stage('Test') {
            steps {
                withMaven(maven: MAVEN_INSTALLATION, mavenSettingsConfig: MAVEN_SETTINGS_CONFIG) {
                    bat 'mvn test'
                }
            }
        }
    }
}
