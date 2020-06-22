These commands can be found on the ECR Page in the AWS Management Console, the button "VIEW PUSH COMMANDS", to push the custom image on the ECR:

aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin 529448940572.dkr.ecr.ap-south-1.amazonaws.com

docker build -t aman/nodejs-test .

docker tag aman/nodejs-test:latest 529448940572.dkr.ecr.ap-south-1.amazonaws.com/aman/nodejs-test:latest

docker push 529448940572.dkr.ecr.ap-south-1.amazonaws.com/aman/nodejs-test:latest

Steps to pull an Image from ECR:

For pulling the docker image from the ECR, we need to cretae a secrets in Kubectl via DockerHub ID, Please find the command below:
kubectl create secret docker-registry regcred --docker-server=user-id.dkr.ecr.ap-south-1.amazonaws.com/repo-name --docker-username=username --docker-password=jahsgdbhtybsaj

This will create a Secret which will help Pull image from the ECR.
*user-id.dkr.ecr.ap-south-1.amazonaws.com/repo-name = ECR Server Id

**horizontalpodautoscaler can be used to autoscale on the basis of the CPU only, the Memory BAsed Autoscaling is still in Beta.

