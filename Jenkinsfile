node{

    stage('SCM Checkout')
    {
       bat 'https://github.com/raviteja2044/online.git'
    }
    
    stage('Run Docker Compose File')
    {
        bat 'sudo docker-compose build'
        bat 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            bat "docker login -u 2044raviteja -p ${DHPWD}"
        }
        bat 'docker push raviteja2044/online'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             bat 'sudo docker login -u "2044raviteja" -p "Ravi@2044" docker.io'
             //bat 'sudo docker push upasanatestdocker/mysql'
             //bat 'sudo docker push upasanatestdocker/job1_web1.0'
             bat 'sudo docker push upasanatestdocker/job1_web2.0'
            // bat 'docker push upasanatestdocker/mysql'
          
    }
}
