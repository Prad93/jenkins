node {
    checkout scm

    docker.withRegistry('', 'dockerhub') {

        def customImage = docker.build("prad93/dockerwebapp:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
