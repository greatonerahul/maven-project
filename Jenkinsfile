node{      
      stage('scm checkout') {
          echo "you are building env.BRANCH_NAME"
          git url: "https://github.com/greatonerahul/simple-java-maven-app.git"
         }      
      if(env.BRANCH_NAME == 'stg'){        
                stage('build'){
                  sh """
                  mvn --version
                  mvn clean package
                  """
                }
            }
            else{
                  echo "you are not entitled to build any other branch then ${params.Branch}"
                  return
                }
        }
