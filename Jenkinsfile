pipeline{
agent any
  tools{
    maven 'Maven'
  }
  stages{
    stage('Checkout'){
      steps{
        git branch:'main',url:'https://github.com/chinmayiii/simplemavenvedio.git'
      }
    }
    stage('Build'){
      steps{
        sh 'mvn clean package'
      }
    }
    stage('Test'){
      steps{
        sh 'mvn test'
      }
    }
    stage('Run Application'){
      steps{
        sh 'java -jar target/2023Simplemavenlist-1.0-SNAPSHOT.jar'
      }
    }
  }
  post{
    success{
      echo 'Build and deployment succesfull'
    }
    failure{
      echo 'Build failed'
    }
  }
}
