pipeline {
    agent any
    stages{
        stage('Checkout') {
            steps{
                gitbranch: 'main', url: 'https://github.com/<student-username>/<repo-name>.git'
            }
        }
        stage('InstallDependencies') {
            steps{
                bat 'pipinstall-rrequirements.txt'
            }
        } 
        stage('RunUnitTests'){
            steps{
                bat 'pytesttest_app.py'
            }
        }
    }
}