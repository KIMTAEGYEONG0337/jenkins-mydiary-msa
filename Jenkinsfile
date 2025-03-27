node {
        stage('Clone repository') {
                git credentialsId: 'github_access_token', url: 'https://github.com/KIMTAEGYEONG0337/jenkins-mydiary-msa.git'
        }

        stage('Build Image') {
                dockerImage = docker.build("offerall0337/mydiary-front:2.0")
        }

        stage('Push Image') {
                withDockerRegistry([ credentialsId: "docker-access", url: "" ]) {
                dockerImage.push()
                }
        }
}

