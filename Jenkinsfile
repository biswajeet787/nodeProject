pipeline {
   agent any

   stages {
       stage('Build') {
           steps {
               sh 'node index.js'
           }
       }

       stage('Test') {
           steps {
               echo 'Running Tests...................................'
           }
       }

       stage('Test2') {
           steps {
               echo 'Running Tests 2...................................'
           }
       }
   }
}


// pipeline {

//     agent any

//     stages {

//         stage('Build Stage') {

//             steps {

//                 sh 'npm install'

//             }
//         }
//         stage('Deploy Stage') {

//             steps {

//                 sh '''

//                 /usr/local/bin/pm2 delete myApp || true

//                 /usr/local/bin/pm2 start index.js --name myApp

//                 /usr/local/bin/pm2 save

//                 '''

//             }
//         }
//     }
// }