pipeline{
    agent slave1
    tools {
        maven "maven3.9.7"
    }
    stages{
        stage('clonefromsourcecode'){
            steps{
                sh "echo 'clone latest code'"
                sh "echo 'build developing for dev environment'"
                git ' https://github.com/Robinpreet98/liontech-web-app-jenkins-cicd-1.git'
            }
        stage('Test+build+package')
        {
            steps{
                 sh "mvn install"
                 sh "mvn validate"
                 sh "mvn test"
                 sh "mvn package"
            }
        }
            
    }
    }
}