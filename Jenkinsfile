pipeline {
    agent { label 'spc' }
    parameters {
        choice(name: 'MAVEN_GOAL' choices [ 'package', 'clean package' ], description: 'this is maven goal')

    }
    stages {
        stage('git') {
            git url: 'https://github.com/sangameshwar-0109/dummy-reposotory-april-24.git',
                branch: 'main' 
        }
    }
    stage('build') {
        steps {
            sh "mvn $(parms.MAVEN_GOAL)"
        }
    }

}
