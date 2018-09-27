pipeline{
    agent any
    
    stages{
        stage('checkout'){
            steps{
                git branch: 'master', url: 'https://github.com/MaxCCC/temp.git'
            }
        }
        
        stage('test'){
            when { 
                changeset "*.yaml" 
            }
            steps{
                echo "The file did change in the last commit (SCM checking)"
            }
        }
    }
}
