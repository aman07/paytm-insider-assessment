YE sab commands ECR ke page pr likhi hoti hai, the button "VIEW PUSH COMMANDS" shows these

aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin 529448940572.dkr.ecr.ap-south-1.amazonaws.com
docker build -t aman/nodejs-test .
docker tag aman/nodejs-test:latest 529448940572.dkr.ecr.ap-south-1.amazonaws.com/aman/nodejs-test:latest
docker push 529448940572.dkr.ecr.ap-south-1.amazonaws.com/aman/nodejs-test:latest