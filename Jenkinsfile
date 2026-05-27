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
       stage('Build') {
           steps {
               sh 'npm install'
           }
       }
       stage('Deploy') {
           steps {
               sh '''
               pm2 delete myapp || true
               pm2 start index.js --name myapp
               '''
           }
       }
   }
}