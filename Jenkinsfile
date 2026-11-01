pipeline {
    agent any 

    stages {
        stage('Clone') { 
            steps {
                // Clones the portfolio repository into the local Jenkins workspace
                git branch: 'main', url: 'https://github.com/TEJASSUSHANTH/Tejas-Sushanth-DevOps-Portfolio-customized-test.git'
            }
        }
        
        stage('Package') { 
            steps {
                // Switches context into the subfolder containing pom.xml to prevent MissingProjectException
                dir('Demo-java-main') {
                    sh 'mvn clean package'
                }
            }
        }
        
        stage('Deploy') { 
            steps {
                echo "Deploying application to Apache Tomcat server..."
                
                // Targets the generated WAR package inside the project directory and moves it to Tomcat
                dir('Demo-java-main') {
                    sh 'cp target/my-java-app-1.0-SNAPSHOT.war /home/ubuntu/apache-tomcat-10.1.61/webapps/'
                }
            }
        }
    }
}
