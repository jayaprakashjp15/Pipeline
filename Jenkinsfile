pipeline
 {
    agent any

    stages 
{
       stage ('clone sources') {
        steps {
        git url: 'https://github.com/RavitejaAdepudi/javawar.git'
        }
       }
        stage ('Compile Stage') 
{

            steps
 {
               
                    sh 'mvn -f pom.xml clean install'
                
            }
        }

        stage ('Testing Stage')
 {

            steps
 {
                
                    sh 'mvn -f pom.xml test'
                }
            
        }
        stage('Deploy to Tomcat')
{
        steps
 {
        sh 'cp -r /root/.jenkins/workspace/Pipeline/mavewebappdemo/target/* /opt/apache-tomcat-8.5.3/webapps/'
        }
        }


        
    }
}
