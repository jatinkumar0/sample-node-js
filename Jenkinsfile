pipeline 
{
agent any
  stages 
  {
    
    
    stage ('Build')
    {
      steps {
      sh 'npm install'    
      }
   }
    stage ('Deploy')
    {
      steps {
        sh '''
        nohup npm run start:dev&
        '''
      }
   }
  
  
  
  
  
  }

}
