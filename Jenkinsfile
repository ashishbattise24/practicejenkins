def gv
pipeline{
 agent any
 
 parameters{
            choice(name: 'VERSION', choices: ['1.2.3', '1.2.4' ,'1.2.5'], description: 'Version choises' )
            booleanParam(name: 'execValue', defaultValue: true, description: 'Boolean parameter')
 }
 stages{
    stage('Init'){
              steps{
                 script{
                  gv = load "buildapp.groovy"
                       }
                   }
    }
    stage('Build'){
    
                steps{
                    script{
                       echo "Building an Application"
                       gv.buildApp()
                          }
                    }
 
                 }
    stage('Test'){
                 steps{

                    script{
                          echo "Testing an App"
                          gv.testApp()
                            }
                      }
                  }
 

}
}
