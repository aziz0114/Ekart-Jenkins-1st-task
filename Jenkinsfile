pipeline {
    agent any

    tools {
        jdk 'jdk 17'
        maven 'maven 3'
    }

    stages {
        stage('Git') {
            steps {
                git branch: 'main', url: 'https://github.com/sawsansalah/Ekart.git'
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        
        stage('Package') {
            steps {
                sh 'mvn package -DskipTests' 
            }
        }
    }
}
