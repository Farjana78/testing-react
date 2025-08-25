pipeline {
     agent any
     
     stages {
          stage('Checkout') {
               steps {
                    git url: 'https://github.com/Farjana78/testing-react.git', branch: 'master'
               }
          }
          
          stage('Build') {
                steps {
                     sh 'sudo npm install'
                     sh 'sudo npm run build'
                }
          }
          
          stage('Deploy') {
               steps {
                    sh '''
                    sudo rm -rf /var/www/html/testing-react/*
                    sudo cp -r build/* /var/www/html/testing-react/
                    '''
               }
          }
     }
}
