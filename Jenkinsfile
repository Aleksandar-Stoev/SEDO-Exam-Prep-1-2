pipeline{
    agent any
    stages{
        stage("Restore dependencies"){
            when {
                anyОf {
                    branch 'main'
                    branch 'master'
                }
            }
            steps{
                bat 'dotnet restore'
            }
        }
        stage("Build the app"){
            when {
                anyОf {
                    branch 'main'
                    branch 'master'
                }
            }
            steps{
                bat 'dotnet build --no-restore'
            }
        }
        stage("Run the tests"){
            when {
                anyОf {
                    branch 'main'
                    branch 'master'
                }
            }
            steps{
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
