node{

    stage('SCM Checkout')
    {
        git credentialsId: '4cc785e9-441d-4818-a248-2bfb2148004d', url: 'https://github.com/VardhanNS/phpmysql-app.git'
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
        bat 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             bat 'sudo docker login -u "upasanatestdocker" -p "Zephyr@17" docker.io'
             //bat 'sudo docker push upasanatestdocker/mysql'
             //bat 'sudo docker push upasanatestdocker/job1_web1.0'
             bat 'sudo docker push upasanatestdocker/job1_web2.0'
            // bat 'docker push upasanatestdocker/mysql'
          
    }
}
