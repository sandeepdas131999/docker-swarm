node ('web') {

         def app

stage ('clone repository') {

             checkout scm

}

stage ('Docker build') {

        sh 'docker build -t sandeep131999

}

stage('push image') {
             withDockerregistry([ credentialsId: "e61d4e00-c2b7-413f-9af9-09dd968f5142", url: '']){
             sh "docker push sandeepdas131999/nginx"
             }

stage ('Docker deploy') {
             sh 'docker service create --name webpage -p 8050:80 sandeepdas131999/nginx'

}
