#!groovy 
#! 1 Get the code from GitHub
#! 2 Install the different dependencies by calling the npm install
#! 3 Run our run with the command mocha
#! 4 Clean up
node {
   stage 'Checkout'
        checkout scm

   stage 'Setup'
        sh 'npm install'

   stage 'Mocha test'
        sh './node_modules/mocha/bin/mocha'

   stage 'Cleanup'
        echo 'prune and cleanup'
        sh 'npm prune'
        sh 'rm node_modules -rf'
}
