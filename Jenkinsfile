pipeline{
   agent any
   tools{
       gradle 'Gradle'
       jdk 'jdk'
       }
    stages{
         stage('Checkout'){
           steps{
            git branch:'master',
                url:'https://github.com/Ranjana2225/gradle-app-02.git'
         }
         }
        stage('Build'){
          steps{
            sh 'gradle build'
          }
        }
      stage('Test'){
        steps{
          sh 'gradle test'
        }
      }
      stage('Run application'){
        steps{
          sh 'gradle run'
        }
      }
    }
  post{
    success{
      echo 'build and deployment succesful'
    }
    failure {
      echo 'build failed'
    }
  }
}
        
