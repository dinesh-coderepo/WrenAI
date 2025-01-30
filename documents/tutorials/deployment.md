# Deployment Tutorial for WrenAI

This tutorial will guide you through the process of deploying the WrenAI project. Follow the steps below to set up the deployment environment, configure the deployment settings, and deploy the project.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- **Docker**: Latest version
- **Kubernetes**: Latest version
- **kubectl**: Latest version
- **Helm**: Latest version

## Step 1: Set Up the Deployment Environment

1. **Clone the Repository**:

   ```sh
   git clone https://github.com/dinesh-coderepo/WrenAI.git
   cd WrenAI
   ```

2. **Create a Namespace**:

   ```sh
   kubectl create namespace wren
   ```

3. **Deploy Secrets**:

   Modify the `secret-wren_example.yaml` file to include your OpenAI API keys and PostgreSQL URL.

   ```sh
   kubectl apply -f deployment/kustomizations/examples/secret-wren_example.yaml -n wren
   ```

## Step 2: Configure the Deployment Settings

1. **Modify Configuration Files**:

   Adjust the values in the `deployment/kustomizations` folder to fit your Kubernetes environment. This includes modifying the `kustomization.yaml` file and any other relevant configuration files.

2. **Inflate the Manifest with Kustomization**:

   ```sh
   kubectl kustomize deployment/kustomizations --enable-helm > deployment/kustomizations/wrenai.kustomized.yaml
   ```

## Step 3: Deploy the Project

1. **Deploy the Inflated Kustomized App**:

   ```sh
   kubectl apply -f deployment/kustomizations/wrenai.kustomized.yaml
   ```

2. **Verify the Deployment**:

   Check the status of the pods to ensure they are running correctly.

   ```sh
   kubectl get pods -n wren
   ```

## Common Issues and Solutions

### Issue: Pods Not Starting

**Solution**: Ensure that all required environment variables are set correctly in the `secret-wren_example.yaml` file. Verify that Docker and Kubernetes are running on your machine.

### Issue: Configuration Errors

**Solution**: Double-check the configuration files in the `deployment/kustomizations` folder. Ensure that all values are set correctly and that there are no syntax errors.

### Issue: Deployment Failures

**Solution**: Review the logs of the failed pods to identify the cause of the failure. Use the `kubectl logs` command to view the logs.

```sh
kubectl logs <pod-name> -n wren
```

## Additional Resources

For more information on deploying WrenAI, refer to the following resources:

- [Kubernetes Documentation](https://kubernetes.io/docs/home/)
- [Docker Documentation](https://docs.docker.com/)
- [Helm Documentation](https://helm.sh/docs/)

We appreciate your contributions and look forward to working with you!
