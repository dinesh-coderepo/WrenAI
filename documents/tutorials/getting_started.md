# Getting Started with WrenAI

Welcome to the WrenAI repository! This tutorial will guide you through the process of setting up your development environment and running the project locally.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- **Python**: Version 3.12 or higher
- **Node.js**: Version 18 or higher
- **Poetry**: Version 1.8.3
- **Just**: Version 1.36 or higher
- **Docker**: Latest version

## Step 1: Clone the Repository

First, clone the WrenAI repository to your local machine:

```sh
git clone https://github.com/dinesh-coderepo/WrenAI.git
cd WrenAI
```

## Step 2: Set Up the Development Environment

### For Wren AI Service

1. **Navigate to the wren-ai-service directory**:

   ```sh
   cd wren-ai-service
   ```

2. **Install dependencies**:

   ```sh
   poetry install
   ```

3. **Generate configuration files**:

   ```sh
   just init
   ```

   This will create both `.env.dev` and `config.yaml` files. Edit these files to set the necessary environment variables and configurations.

4. **Start the required containers**:

   ```sh
   just up
   ```

5. **Launch the AI service**:

   ```sh
   just start
   ```

### For Wren UI

1. **Navigate to the wren-ui directory**:

   ```sh
   cd ../wren-ui
   ```

2. **Install dependencies**:

   ```sh
   yarn install
   ```

3. **Run the development server**:

   ```sh
   yarn dev
   ```

## Step 3: Access the Application

Open your browser and navigate to `http://localhost:3000` to access the WrenAI application.

## Common Issues and Solutions

### Issue: Docker Containers Not Starting

**Solution**: Ensure Docker is running on your machine. If the containers still do not start, try restarting Docker and running the `just up` command again.

### Issue: Dependencies Not Installing

**Solution**: Ensure you have the correct versions of Python, Node.js, Poetry, and Just installed. If you encounter errors during installation, try updating these tools to their latest versions.

### Issue: Environment Variables Not Set

**Solution**: Double-check your `.env.dev` and `config.yaml` files to ensure all required environment variables are set correctly. Refer to the `.env.example` files for guidance.

### Issue: Application Not Accessible

**Solution**: Ensure the development servers for both Wren AI Service and Wren UI are running. Check the terminal output for any errors and resolve them as needed.

## Next Steps

Once you have the development environment set up and the application running locally, you can start exploring the codebase and contributing to the project. Refer to the [Contributing Guide](../contributing.md) for more information on how to contribute.

Happy coding!
