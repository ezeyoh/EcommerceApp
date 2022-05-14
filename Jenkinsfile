node{

    stage('SCM Checkout')
    {
        git credentialsId: 'e0305a37-1bd4-4ffc-988d-ffc96c362edf', url: 'https://github.com/ezeyoh/EcommerceApp.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u upasanatestdocker -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "ezeyoh.deriv@gmail.com" -p "56727882Eb@" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push ezeyoh321/ecommproject'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
