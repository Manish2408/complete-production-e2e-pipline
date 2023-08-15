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
     }
    
        stages("Checkout from SCM"){
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/Manish2408/complete-production-e2e-pipline.git'
            }

        }
}
