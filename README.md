These commands can be found on the ECR Page in the AWS Management Console, the button "VIEW PUSH COMMANDS", to push the custom image on the ECR:

aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin 529448940572.dkr.ecr.ap-south-1.amazonaws.com

docker build -t aman/nodejs-test .

docker tag aman/nodejs-test:latest 529448940572.dkr.ecr.ap-south-1.amazonaws.com/aman/nodejs-test:latest

docker push 529448940572.dkr.ecr.ap-south-1.amazonaws.com/aman/nodejs-test:latest
