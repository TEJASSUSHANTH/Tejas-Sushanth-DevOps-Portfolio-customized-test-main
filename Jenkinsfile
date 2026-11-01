
stage('clone') { 
    steps {
        git branch: 'main', 
            credentialsId: '3ac4cf0e-8609-4580-85d4-5baa695eb4c3', 
            url: 'https://github.com/TEJASSUSHANTH/Tejas-Sushanth-DevOps-Portfolio-customized-test-main.git'
    }
}

        stage('package') { 
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo "i am Deploying"'
                //sh 'sudo cp /var/lib/jenkins/workspace/pipelineJob/target/my-java-app-1.0-SNAPSHOT.war /home/ubuntu/apache-tomcat-10.1.61/webapps/'
            }
        }
    }
}
