pipeline {

  agent any
  
  parameters{
    text(name: 'nombre', description: 'nombre', defaultValue: 'nombre')
    string(name:'apellidos', description: 'apellidos', defaultValue: 'apellidos')
    choice(name: 'edad', description: 'edad', choices: '16\n17\n18')
  }
  
  stages{
  
    stage("Saludo") {
      
      steps{
    
      script{
   
        groovySaludo = load("groovy/saludo.groovy")
        groovySaludo.saludo(${apellidos})

        
        
          } // END Scripts
      } // END Streps
    } // END Stage Saludo
  
  
  }
  post {
    
    always{
      script{
      env.saludo = "saludo desde pipelin"
      }
      }
  
    success { 
      echo "Success"
    }
    
    failure {
      echo "Failure"
    }
    
    aborted {
      echo "Aborted"
    }
  
  }
  
  
}
