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

       stage('Test') {
           steps {
               sh 'node index.js &'
               sh 'sleep 5'
               sh 'curl http://localhost:3000'
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
