pipeline{
        agent any;
        stages{
                stage('SCM Checkout'){
                        steps{
                                git branch: 'main', credentialsId: 'medal-cred', url: 'https://github.com/MedalMan/CloudFlyers.git'
                        }

                }
                stage('Build Docker Image'){
                        steps{
                                sh 'docker build -t medalman/mydockerrepo:latest .'
                        }
                }
                stage('Push Docker Image'){
                        steps{
                            sh 'docker login -u medalman -p Eteyen@1983'
                            sh 'docker push medalman/mydockerrepo:latest'
                        }

                }
        }
}
