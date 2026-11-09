pipeline
{
    agent any
    stages
    {
        stage('download')
        {
            steps
            {
                git 'https://github.com/IntelliqDevops/maven.git'
            }
        }
        stage('build')
        {
            steps
            {
                sh 'mvn package' 
            }
        }
        stage('deployment')
        {
            steps
            {
                sh 'scp /var/lib/jenkins/workspace/DeclarativePipeline2/webapp/target/webapp.war ubuntu@172.31.31.141:/var/lib/tomcat10/webapps/testapp.war'
            }
        }
    }
}
