pipeline{
  agent any
  stages{
    stage ('checkout'){
      steps{
        bat 'git clone https://github.com/jloisel/angularjs-helloworld.git'
        bat 'dir'
        bat 'cd angularjs-helloworld'
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
