// pipeline {
// 	agent any
//     stages {
//         stage('Build on k8 ') {
//             steps {           
//                         sh 'pwd'
//                         sh 'cp -R helm/* .'
// 		        sh 'ls -ltr'
//                         sh 'pwd'
//                         sh '/usr/local/bin/helm upgrade --install petclinic-app petclinic --set image.repository=registry.hub.docker.com/dibangoxx/petclinic --set image.tag=1'
              			
//             }           
//         }
//     }
// }



pipeline {
    agent any
    stages {
        stage('Build on k8') {
            steps {
                // Print current directory
                sh 'pwd'

                // Copy Helm chart files from helm directory to current directory
                sh 'cp -R helm/* .'

                // List files in the current directory
                sh 'ls -ltr'

                // Print current directory again
                sh 'pwd'

                // Execute Helm upgrade command to install or upgrade the Helm chart
                sh '/usr/local/bin/helm upgrade --install petclinic-app petclinic --set image.repository=registry.hub.docker.com/dibangoxx/petclinic --set image.tag=1'
'

            }
        }
    }
}
