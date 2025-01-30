# Architecture of WrenAI

## Overview

WrenAI is an open-source GenBI AI Agent that empowers data-driven teams to chat with their data to generate Text-to-SQL, charts, spreadsheets, reports, and BI. It integrates with various LLM models and provides a seamless end-to-end workflow for data analysis and visualization.

## Components

WrenAI consists of the following main components:

### Wren AI Service

The Wren AI Service processes queries using a vector database for context retrieval, guiding LLMs to produce precise SQL outputs. It is responsible for the core AI functionalities, including text-to-SQL conversion, SQL breakdown, and SQL generation reasoning.

### Wren UI

The Wren UI is an intuitive user interface for asking questions, defining data relationships, and integrating data sources. It provides a user-friendly platform for interacting with the AI service and visualizing the results.

### Wren Engine

The Wren Engine serves as the semantic engine, mapping business terms to data sources, defining relationships, and incorporating predefined calculations and aggregations. It ensures that the AI service has the necessary context to generate accurate SQL queries.

## Interactions

The interactions between the different components of WrenAI are as follows:

1. **User Interaction**: Users interact with the Wren UI to ask questions and define data relationships.
2. **Query Processing**: The Wren UI sends the user queries to the Wren AI Service for processing.
3. **Context Retrieval**: The Wren AI Service retrieves the necessary context from the vector database.
4. **SQL Generation**: The Wren AI Service generates the SQL query based on the retrieved context and the user's question.
5. **Semantic Mapping**: The Wren Engine provides the necessary semantic mapping to ensure the generated SQL query is accurate.
6. **Result Visualization**: The Wren UI displays the results of the SQL query to the user.

## Design Patterns

WrenAI uses several design patterns to ensure modularity, scalability, and maintainability:

1. **Microservices Architecture**: Each component of WrenAI is designed as a microservice, allowing for independent development, deployment, and scaling.
2. **Model-View-Controller (MVC)**: The Wren UI follows the MVC pattern to separate the user interface, business logic, and data access layers.
3. **Dependency Injection**: The Wren AI Service and Wren Engine use dependency injection to manage dependencies and promote loose coupling between components.
4. **Observer Pattern**: The Wren AI Service uses the observer pattern to notify components of changes in the state, ensuring real-time updates and synchronization.

## Diagrams

The following diagrams illustrate the architecture and interactions between the components of WrenAI:

### Architecture Diagram

![Architecture Diagram](../misc/architecture_diagram.png)

### Interaction Diagram

![Interaction Diagram](../misc/interaction_diagram.png)

These diagrams provide a visual representation of the architecture and interactions, helping to understand the flow of data and the relationships between the components.

## Conclusion

The architecture of WrenAI is designed to provide a robust and scalable solution for data-driven teams to interact with their data using natural language. By leveraging various design patterns and a microservices architecture, WrenAI ensures modularity, scalability, and maintainability, making it a powerful tool for data analysis and visualization.
