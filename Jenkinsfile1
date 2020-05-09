pipeline
{
agent any
environment
{
PATH = "/Library/Frameworks/Python.framework/Versions/3.8/bin:$PATH"
}
stages
  {
   stage('Git checkout')
   {
   steps
   {
   git credentialsId: 'github', url: 'https://github.com/Aditi-22/PyMath'
   }
   }
   stage("Python Build")
   {
   steps
   {
   sh "python3 math_func.py"
   }  
   }
  }
}
