pipeline

{
  agent any
  tools 
  {
      Python ‘Python3’
  }
  stages 
  {
      stage ('Initialize') 
      {
          steps
          {
              sh '''
              echo "PATH = ${PATH}"
              '''
          }

      }
       stage('Message')
       {
           steps
           {
               echo 'Job started'
           }

        }

           stage ('Build') 

           {

            steps {
                    sh 'python3 math_func.py'


                
            }
           stage (‘TestandPackage’) 

           {

            steps {

                //to test and package the project
                   sh 'python3 test_math_func.py'


                //packaging

                sh 'pyinstaller math_func.py’

            }
          }

       }

}
