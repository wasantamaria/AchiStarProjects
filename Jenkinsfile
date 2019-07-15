node {
    def app
    def registry

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
        registry = "wasantamaria/achistar-1"
        app = docker.build registry + ":$BUILD_NUMBER"
    }

}
