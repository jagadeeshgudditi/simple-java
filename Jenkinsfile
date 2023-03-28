pipeline {
 agent any
     stages {
         stage('Clone Repository') {
         /* Cloning the repository to our workspace */
         steps {
         checkout scm
         }
    }
    stage('Build Image') {
         steps {
         sh 'docker build -t javaapp:v1 .'
         }
    }
    stage('Run Image') {
         steps {
         sh 'docker run -d -p 8050:8000 --name javaapp reactapp:v1'
         }
    }
    stage('Testing'){
         steps {
             echo 'Testing..'
             }
    }
    }
}
