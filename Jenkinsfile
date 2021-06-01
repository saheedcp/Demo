node{

    stage('SCM Checkout')
    {
        git credentialsId: 'github', url: 'https://github.com/saheedcp/Demo.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh ' docker-compose build'
        sh ' docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u saheed3828 -p ${DHPWD}"
        }
        sh 'docker push saheed3828/job1_web2.0'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh ' docker login -u "saheed3828" -p "saheed@120" docker.io'
            
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh ' docker push saheed3828/job1_web2.0'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
