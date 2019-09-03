// Declarative //
pipeline {
agent {
docker { hello-world 'node:helloworld' }
}
stages {
stage('Test') {
steps {
sh 'node --version'
}
}
}
}
// Script //
node {
/* Requires the Docker Pipeline plugin to be installed */
docker.hello-world('node:helloworld').inside {
stage('Test') {
sh 'node --version'
}
}
}
