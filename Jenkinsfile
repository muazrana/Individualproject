pipeline{
        agent any
        stages{ 
		stage('---Build_Image---'){
			steps{
                        	sh label: '1', script: "cd ./Flask_App && sudo docker build -t flask-app ."
                        }
                }
                stage('---clean---'){
                        steps{
                              sh label: '', script: '''if [ "$(sudo docker ps -q -f name=flask-app)" ]; then
    					#cleanup
					sudo docker rm -f flask-app
    				fi'''
   			 }
		}	
		stage('---Build_Container---'){  
			steps{		
				sh "sudo docker run -d --name flask-app -p 5000:5000 flask-app"
				
                        }
                }
        }
}
