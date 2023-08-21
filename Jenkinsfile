pipeline{
    agent{
        label "jenkins-agent"
    }
    tools {
        jdk 'Java17'
        maven 'Maven3'
    }
     stages{
        stage("Cleanup Workspace"){
            steps {
                cleanWs()
            }

        }
        stage("Checkout from SCM"){
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/Manish2408/complete-production-e2e-pipline.git'
            }

        
        }
        stage("Build Applictaion"){
            steps {
                sh "mvn clean package"
            }

        
        }
        stage("test Application"){
            steps {
                sh "mvn test"
            }

        
        }


        }
}
