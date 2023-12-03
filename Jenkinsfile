pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                script {
                    echo 'initializing'
                }
            }
        }
        stage("build app") {
            steps {
                script {
                    echo "building app"
                    
                }
            }
        }
        stage("build image") {
            steps {
                script {
                    echo "building image"
                    
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    echo "deploying"
                    def ssh = 'docker run -d -p 3000:80 gbaderobusola/busola:my-app-1.1'
                    sshagent(['Ubuntu-SSH']) {
                         sh "ssh -o StrictHostKeyChecking=no ubuntu@100.25.183.255 ${ssh}"
                        }
                    
                }
            }
        }
    }   
}
