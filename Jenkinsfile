pipeline {
        agent any
  tools {maven 'maven2'}
    }
    stages{
        stage("Checkout"){
            steps{
                echo "starting the checkout"
                git url: 'https://github.com/myitportal/DevOpsClassCodes.git'
                echo "checkout"
            }
        }
        stage("scr-code-compile"){
            steps{
                echo "here code would be converted from user readable launguage to machine readable launguage"
                bat "mvn compile"
            }
        }
        stage("scr-code-test"){
            steps{
                echo "here the testing of the project will happen from the testcases"
                bat "mvn test"
            }
        }
        stage("scr-code-qa"){
            steps{
                echo "here the code review would be done via pmd"
                bat "mvn pmd:pmd"
            }
        }
        stage("scr-code-package"){
            steps{
                echo "here the code would be converted to the package or executable file"
                bat "mvn package"
            }
        }
    }
