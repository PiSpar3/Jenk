pipeline{
    agent any
    stages{
        stage("Testing"){
            steps{
                sh """
                        echo "Welcome to Jenkins Ola"
                   
                   """
            }
        }

    stage("Deploy"){
           stage{
               sh """
                       echo "welcome to the Deployment. Added jenkins"
                       ssh -o StrictHostKeyChecking=no -T -i /var/lib/jenkins/jenkfile.pem ubuntu@ec2-52-91-106-32.compute-1.amazonaws.com
                       sudo apt update -y
                       cd /var/www
                       sudo rm -rf html
                       git clone https://github.com/PiSpar3/jenk.git html
                   """    
           }
        }
    }
}