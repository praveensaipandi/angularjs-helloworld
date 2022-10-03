pipeline{
  agent any
  stages{
    stage ('checkout'){
      steps{
       bat 'git pull origin master'
       }
     }
    stage ('install modules'){
      steps{
        bat 'npm install --verbose -d' 
        bat  'npm install --save classlist.js'
      }
    }
    stage ('build') {
      steps{
        bat 'ng build --prod --build-optimizer'
      }
    }
  }
}
