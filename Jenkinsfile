pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
				git 'https://github.com/Nitisha230986/coe-poc-repository.git'
                                bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
				git 'https://github.com/Nitisha230986/coe-poc-repository.git'
				bat "mvn -Dmaven.test.failure.ignore=true clean test"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
				git 'https://github.com/Nitisha230986/coe-poc-repository.git'
				bat "mvn -Dmaven.test.failure.ignore=true clean deploy -DmuleDeploy"
            }
        }
    }
}
