pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh "mvn clean package"
            }
        }
        stage('Deploy'){
            steps{
                deploy adapters: [tomcat8(credentialsId: '42854093-ee42-4a9c-bf57-dc18c3b919e0', path: '', url: 'http://ec2-3-110-49-252.ap-south-1.compute.amazonaws.com:8080/')], contextPath: 'javawebproject', war: '**/java-web-project.war'
            }
        }
    }
}
