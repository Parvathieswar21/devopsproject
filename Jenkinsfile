pipeline {
agent any


tools {
    jdk 'JDK17'
    maven 'Maven3'
}

stages {

    stage('Checkout') {
        steps {
            git branch: 'main',
            url: 'https://github.com/Parvathieswar21/devopsproject.git'
        }
    }

    stage('Build') {
        steps {
            bat 'mvn clean package -DskipTests'
        }
    }

    stage('Test') {
        steps {
            bat 'mvn test'
        }
    }
}

post {
    always {
        echo 'Pipeline completed.'
    }
}

}
