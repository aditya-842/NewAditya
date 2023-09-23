pipeline {
					
					agent any
					
					tools {
						maven "mvn"
					}
					stages {
						stage('Stage 1 - Checkout Code') {
							steps {
								//Get the code form GITHUB							
                                echo "https://github.com/ajautomation/PassParametersRunTimeViaMVN"
							}
						}
						stage('Stage 2 - Compile Code') {
							steps {
								//cmd to compile the code							
                                echo "mvn compile"
                                //sh "mvn compile"
							}
						}
						stage('Stage 3 - Run Unit Tests') {
							steps {
								//cmd to run tests							
                                echo "mvn test"
							}
						}
						stage('Stage 4 -Create build') {
							steps {
								//cmd to create the build of project							
                                echo "mvn testpackage"
							}
						}
	
					}
					post{
					    	failure {
						//Send email to team about the failure
						//emailext body: 'Jenkins build failed', subject: 'Jenkins build failed', to: 'test1@test.com'
					
					        echo "Email sent for Jenkins build failed"
				         }
					}
				
					
				}
