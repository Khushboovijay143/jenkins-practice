pipeline {
    agent { node { label 'Agent' } } 

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
              sh '''
                ls -ltr
                pwd
                echo "Hello From Github Push Webhook Event"
              '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post { 
        always { 
            echo 'I will always say whether the job is success or not'
        }
        success{
            echo 'I will only run when the job is success'
        }
        failure{
            echo 'I will only run when the job is failure'
        }
    }
}