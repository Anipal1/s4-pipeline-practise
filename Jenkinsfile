pipeline {
    agent {
     label ("node1 || node2 ||  node3 || node4 ||  node5 ||  branch ||  main ||  jenkins-node || docker-agent ||  jenkins-docker2 ||  preproduction ||  production")
            }

options {
    buildDiscarder(logRotator(numToKeepStr: '20'))
    disableConcurrentBuilds()
    timeout (time: 60, unit: 'MINUTES')
    timestamps()
  }

    stages {
        stage('Setup parameters') {
            steps {
                script {
                    properties([
                        parameters([    
                        
                        choice(
                            choices: ['Dev', 'Sanbox','Prod'], 
                            name: 'Environment'   
                                ),

                          string(
                            defaultValue: 's4user',
                            name: 'User',
			                description: 'Required to enter your name',
                            trim: true
                            ),

                          string(
                            defaultValue: 'eric-001',
                            name: 'DB-Tag',
			                description: 'Required to enter the image tag',
                            trim: true
                            ),

                          string(
                            defaultValue: 'eric-001',
                            name: 'UI-Tag',
			                description: 'Required to enter the image tag',
                            trim: true
                            ),

                          string(
                            defaultValue: 'eric-001',
                            name: 'WEATHER-Tag',
			                description: 'Required to enter the image tag',
                            trim: true
                            ),

                          string(
                            defaultValue: 'eric-001',
                            name: 'AUTH-Tag',
			                description: 'Required to enter the image tag',
                            trim: true
                            ),
                        ])
                    ])
                }
            }
        }
 
        stage('permission') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('cleaning') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('sonarqube') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('build-dev') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('build-sanbox') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }


        stage('build-prod') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('login') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('push-to-dockerhub-dev') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('push-to-dockerhub-sanbox') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('push-to-dockerhub-prod') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('update helm charts-dev') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('update helm charts-sanbox') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('update helm charts-prod') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }

        stage('wait for argocd') {
            steps {
                sh '''
                ls 
                pwd
                '''
            }
        }


        
    }
	
	
	
post {
    
    success {
      slackSend (channel: '#development-alerts', color: 'good', message: "The Job was successful")
    }

    failure {
      slackSend (channel: '#development-alerts', color: '#FF0000', message: "FAILURE: The Job was NOT successful")
    }
}
	
	
}

