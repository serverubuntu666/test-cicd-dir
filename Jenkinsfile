pipeline {
    agent { label "DEV"}
    parameters {
        string(name: 'NAME', description: 'whats your name?')
        booleanParam(name:'SKIP_TEST', description: 'Do you wanna skip test?' )
        choice(name: 'BRANCH', choices: ['master', 'dev'], description:'choose the branch')
        password(name: 'SONAR_SERVER_PWD', description: 'Enter sonar password')
    }


    stages {
        stage('build phase') {
            steps {
                echo "this is a build phase."
            }
        }

        stage('testing phase') {
            steps {
                echo "this is testing phase...."
            }
        }

        stage('deploying phase') {
            steps {
                echo "this is deploying phase...."
            }
        }

        stage('Printing parameters'){
            steps {
                echo "hello ${params.NAME}"
                echo "skip running test:${params.SKIP_TEST}"
                echo "Branch choice: ${params.BRANCH}"
                echo "Sonar password: ${params.SONAR_SERVER_PWD}"
            }
        }
    }
}
