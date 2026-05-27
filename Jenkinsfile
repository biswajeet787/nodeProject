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

       stage('Run') {
           steps {
               sh 'node index.js'
           }
       }

   }
}