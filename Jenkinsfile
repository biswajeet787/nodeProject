// pipeline {
//    agent any

//    stages {
//        stage('Build') {
//            steps {
//                echo 'Building Application'
//            }
//        }

//        stage('Test') {
//            steps {
//                echo 'Running Tests'
//            }
//        }
//    }
// }


pipeline {

    agent any

    stages {

        stage('Build Stage') {

            steps {

                sh 'npm install'

            }
        }

        stage('Deploy Stage') {

            steps {

                sh '''

                sudo pm2 delete myapp || true

                sudo pm2 start index.js --name myapp

                sudo pm2 save

                '''

            }
        }
    }
}
