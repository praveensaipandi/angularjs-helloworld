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
        cd 'C:\ProgramData\Jenkins\.jenkins\workspace\test'
        bat 'npm install --verbose -d' 
      }
    }
    stage ('build') {
      steps{
        cd 'C:\ProgramData\Jenkins\.jenkins\workspace\test'
        bat 'ng build'
      }
    }
  }
}
