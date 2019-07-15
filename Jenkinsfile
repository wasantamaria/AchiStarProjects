node {
    def app
    def registry
    def registryCredential

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
        registry = "wasantamaria/achistar-1"
        registryCredential = ‘dockerhub’
        app = docker.build registry + ":$BUILD_NUMBER"
        app.push()
    }

}
