@Library('Jenkins_Shared_Library') _

pipeline{

    agent any

    stages{
        
        stage('Git Checkout'){

            steps{
            gitCheckout(

                branch: "main",
                url: "https://github.com/Nelgit007/java_app.git"
            )
            }
        }
        stage('Unit test using maven'){

            steps{
                script{

                    mvnTest()
                }
        
            }
        }
        stage('Integration test using maven'){

            steps{
                script{

                    mvnIntegrationTest()
                }
        
            }
        }
    }
}
