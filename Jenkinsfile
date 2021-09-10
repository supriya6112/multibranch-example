pipeline {
    agent { label "master" }
    stages {
        stage('build') {
            steps {
                sh "DOCKER_HOST=tcp://localhost:2375 docker build -t webserver webserver/"
            }
        }


        stage("run")
        {
            steps
            {
                sh "DOCKER_HOST=tcp://localhost:2375 docker run -it --rm -d -p 9000:80 --name webpage4 webserver"
            }
        }
    }
}
