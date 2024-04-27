pipeline {
    agent any
    tools {
        nodejs '22.0.0'
    }
    stages{
        stage("checkout"){
            steps{
                checkout scm
            }
        }

        stage("Test"){
            steps{
                sh 'npm test'
            }
        }

        stage("Build"){
            steps{
                sh 'npm run build'
            }
        }

        // stage("Build Image"){
        //     steps{
        //         script {
        //             dockerIMg = docker.build("ahmedzak7/nodejs2:latest")
        //         }
        // }
        // }
        // stage('Docker Push') {
        //     steps {
        //         withCredentials([usernamePassword(credentialsId: 'docker_cred', passwordVariable: 'DOCKERHUB_PASSWORD', usernameVariable: 'DOCKERHUB_USERNAME')]) {
        //             sh 'docker login -u $DOCKERHUB_USERNAME -p $DOCKERHUB_PASSWORD'
        //             sh 'docker tag my-node-app:1.0 bashidkk/my-node-app:1.0'
        //             sh 'docker push bashidkk/my-node-app:1.0'
        //             sh 'docker logout'
        //         }
        //     }
        // }
    }
}
