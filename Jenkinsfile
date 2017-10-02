pipeline {
    agent { docker 'python:3.5.1' }
    pamemeters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.Greeting}" World!"
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}
