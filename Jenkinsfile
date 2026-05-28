pipeline {
agent any

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

    success {
        echo 'Build Successful'
    }

    failure {
        echo 'Build Failed'
    }

    always {
        echo 'Pipeline completed.'
    }
}


}
