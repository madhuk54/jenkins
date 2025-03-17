pipeline {
    agent any  
    environment {
        JAVA_HOME = "C:\\Program Files\\Java\\jdk-21"  // Update if needed
        PATH = "${JAVA_HOME}\\bin;${env.PATH}"
    }
    stages {
        stage('Clone from GitHub') {
            steps {
                git branch: 'main', url: 'https://github.com/madhuk54/jenkins.git'
            }
        }
        stage('Compile Java') {
            steps {
                bat 'javac HelloWorld.java'  // Compile Java files
            }
        }
        stage('Run Java Program') {
            steps {
                bat 'java HelloWorld'  // Run the Java program
            }
        }
    }
}
