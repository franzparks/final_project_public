pipeline {
    agent any
    
    stages {

        stage("Build Dev Environment") {
            when { branch 'dev' }
            steps {
                /*
                  TODO: find path to test/deployment scripts for dev env
                 */

                echo "terminating existing dev instances just incase"
                
                echo "building new dev instance"

            }
        }
        stage("Run Tests On Dev Site") {
            when { branch 'dev' }
            steps {
              /*
                TODO: run tests on dev server
              */
              echo 'Testing Dev'
            }
        }
        stage("Git merge dev to stage"){
            when { branch 'dev' }
            steps {
                script {
                  /*
                    TODO: merge dev branch into stage
                  */
                  echo 'Merge dev into stage'
                }
            }
        }
        stage("Delete Dev Instance"){
            when { branch 'dev' }
            steps {
                /*
                  TODO: If tests pass on Dev, delete the dev instance.
                  
                 */

                /* Delete dev when the tests pass*/
                echo "terminating dev instance"

            }
        }
        stage("Build Stage Environment") {
            when { branch 'stage' }
            steps {
              echo "TODO: terminating stage instances if they exist"
             
              echo "Building new Stage instance"

              /* wait for at least 5 min for the server to start */

              }

        }
        stage("Run Tests On The Stage Site") {
            when { branch 'stage' }
            steps {
              /*TODO:  Run stage tests */
              echo "Testing Stage"
            }
        }
        stage("Delete Stage Environment"){
            when { branch 'stage' }
            steps {
              /* TODO: Delete stage when the tests pass*/

              echo "terminating stage instance"

            }
        }
        stage("Git Merge stage to master"){
            when { branch 'stage' }
            steps {
             /* TODO: Merge stage branch into master branch*/
                echo "merge stage into master branch"
            }
        }
        stage("Run Tests On The Prod Site") {
            when { branch 'master' }
            steps {
              /*TODO:  Run master tests */
              echo "Testing Production"
            }
        }
        
    }
}
