pipeline {
    agent any 

    stages {
        stage('Package') { 
            steps {
                // Compiles the Java app and packages the WAR file from the root directory
                sh 'mvn clean package'
            }
        }
        
        stage('Deploy') { 
            steps {
                echo "Deploying application to Apache Tomcat server..."
                // Copies the generated WAR package directly to Tomcat's live webapps directory
                sh 'cp target/my-java-app-1.0-SNAPSHOT.war /home/ubuntu/apache-tomcat-10.1.61/webapps/'
            }
        }
    }
}
