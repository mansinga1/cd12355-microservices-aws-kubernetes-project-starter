# Prerequisite
Ensure you run the "buildspec.yml" once the code has been changed and committed to a branch. This will push the latest docker image to ECR.

# How to deploy this application
1. The docker image is stored on ECR and tagged with the latest prefix tag
2. Update the deployment.yaml and push to remote repository, then run "kubectl apply -f deployment.yaml"
3. Once deployed, check the status of the pod with "kubectl get pods" and proceed in a running state
4. Finally deploy your service with "kubectl apply -f service.yaml".

Once all the services are up and running, check the logs for the application pod to know if the container is running successfully.