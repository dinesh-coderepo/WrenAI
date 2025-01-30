# WrenAI Documentation

Welcome to the WrenAI documentation. This repository contains all the necessary information to understand, contribute to, and deploy WrenAI.

## Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
- [Architecture](architecture.md)
- [Contributing](contributing.md)
- [Tutorials](#tutorials)
  - [Getting Started](tutorials/getting_started.md)
  - [Adding a New Feature](tutorials/adding_new_feature.md)
  - [Deployment](tutorials/deployment.md)

## Overview

WrenAI is an open-source GenBI AI Agent that empowers data-driven teams to chat with their data to generate Text-to-SQL, charts, spreadsheets, reports, and BI. It integrates with various LLM models and provides a seamless end-to-end workflow for data analysis and visualization.

## Getting Started

To get started with WrenAI, follow these steps:

1. **Clone the Repository**: Clone the WrenAI repository to your local machine.
   ```sh
   git clone https://github.com/dinesh-coderepo/WrenAI.git
   cd WrenAI
   ```

2. **Install Dependencies**: Install the necessary dependencies for the project.
   ```sh
   # For wren-ai-service
   cd wren-ai-service
   poetry install

   # For wren-ui
   cd ../wren-ui
   yarn install
   ```

3. **Set Up Environment Variables**: Create a `.env` file in the root directory and add the required environment variables. Refer to the `.env.example` files in the respective directories for guidance.

4. **Run the Project Locally**: Start the services locally.
   ```sh
   # For wren-ai-service
   cd wren-ai-service
   just start

   # For wren-ui
   cd ../wren-ui
   yarn dev
   ```

5. **Access the Application**: Open your browser and navigate to `http://localhost:3000` to access the WrenAI application.

## Main Components

WrenAI consists of the following main components:

- **Wren AI Service**: Processes queries using a vector database for context retrieval, guiding LLMs to produce precise SQL outputs.
- **Wren UI**: An intuitive user interface for asking questions, defining data relationships, and integrating data sources.
- **Wren Engine**: Serves as the semantic engine, mapping business terms to data sources, defining relationships, and incorporating predefined calculations and aggregations.

For a detailed explanation of the architecture and interactions between these components, refer to the [Architecture](architecture.md) document.

## Tutorials

We have prepared several tutorials to help you get started and contribute to WrenAI:

- [Getting Started](tutorials/getting_started.md): A step-by-step guide on how to set up the development environment and run the project locally.
- [Adding a New Feature](tutorials/adding_new_feature.md): Instructions on how to add a new feature to the repository, including creating a new branch, making changes, writing tests, and submitting a pull request.
- [Deployment](tutorials/deployment.md): A comprehensive guide on how to deploy the project, including setting up the deployment environment, configuring deployment settings, and troubleshooting common issues.

We hope this documentation helps you understand and contribute to WrenAI. If you have any questions or need further assistance, feel free to reach out to us on [Discord](https://discord.gg/5DvshJqG8Z) or [GitHub Issues](https://github.com/dinesh-coderepo/WrenAI/issues).
