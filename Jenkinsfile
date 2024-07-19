pipeline {
    agent { label 'spc' }
    parameters {
        choice(name: 'MAVEN_GOAL', choices: ['package', 'clean package'], description: 'This is the Maven goal')
    }
    stages {
        stage('git') {
            steps {
                git url: 'https://github.com/sangameshwar-0109/dummy-reposotory-april-24.git',
                    branch: 'main'
            }
        }
        stage('build') {
            steps {
                sh "mvn ${params.MAVEN_GOAL}"
            }
        }
    }
}
