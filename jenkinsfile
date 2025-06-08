pipeline{
   agent any
    tools{
         gradle 'Gradle'
         jdk 'JDK'
    }
    stages{
      stage('checkout'){
            steps{
            git branch:'master',url:'https://github.com/imsudeeppatil/gradle.git'
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
    echo 'Build succcess'
  }
  failure{
   echo'Build failure'
  }
}
}
 
      
