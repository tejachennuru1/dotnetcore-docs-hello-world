pipeline {
    agent { label 'my-defined-label' }

    stages {
        stage('git') {
            steps {
                git branch: 'master', url: 'https://github.com/tejachennuru1/dotnetcore-docs-hello-world.git'
            }
        }
    }

    stage('build') {
            steps {
            sh 'dotnet build'
            sh 'dotnet publish'
            }

            stage('artifacts') {
                steps {
                    archiveArtifacts artifacts:  '**/ package.zip'
                }
            }
    }
}
}}