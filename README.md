# Palo Alto Networks AI Runtime Security Postman Collection

This repository contains a Postman collection for interacting with Palo Alto Networks AI Runtime Security (AIRS) API. Use this collection to automate and streamline your interactions with the AIRS platform.

## Overview

The AI Runtime Security Postman collection provides pre-configured API requests for common operations in the AIRS platform, allowing you to:

- Authenticate to the AIRS API
- Query security insights and findings
- Manage security policies
- Interact with AI model security controls
- Generate reports and analytics

## Getting Started

### Importing the Collection

1. Open Postman and click on "Import" in the top left corner
2. Select "File" > "Upload Files" or simply drag and drop the `AI-Runtime-Security.postman_collection.json` file
3. Click "Import" to add the collection to your workspace

### Setting Up Variables

This collection requires several variables to function properly. You can either:

1. **Update Collection Variables**:
   - Click on the collection name (AI Runtime Security)
   - Go to the "Variables" tab
   - Update the values for each required variable

2. **Create an Environment File** (recommended):
   - Click on "Environments" in the sidebar
   - Click "+" to create a new environment
   - Add the following variables and their values:
     - `apiKey` - Your API authentication key
     - `transactionId` - Unique identifier for tracking requests
     - `profileId` - Target security profile ID
     - `appName` - Application name for targeting
     - `profileName` - Profile name for targeting
     - `appUser` - Application user identifier
     - `aiModel` - AI model identifier
     - `scanId` - Scan operation identifier
     - `reportId` - Report identifier

**Note**: Create separate environments (e.g., dev, staging, prod) to easily switch between different settings.

## Usage

### Running Requests in Postman

1. Select your environment from the dropdown in the top right
2. Navigate to a request in the collection
3. Check the "Pre-request Script" tab to understand what happens before the request
4. Click "Send" to execute the request
5. Examine the "Tests" tab to see the automated validations performed
6. View the response in the lower panel, including:
   - Status code and time
   - Response body
   - Test results

### Visualizing Responses

Many requests include visualizations based on the response data:

1. Send a request
2. Click on the "Visualize" tab in the response section
3. View charts, graphs, and formatted data based on the response
4. Adjust visualization settings using the controls provided

### Running in Newman (Command Line)

Run the entire collection from either CLI or CICD

```bash
# Install Newman globally
npm install -g newman

# Run the entire collection with an environment
newman run AI-Runtime-Security.postman_collection.json -e your-environment.json

# Run a specific folder
newman run AI-Runtime-Security.postman_collection.json -e your-environment.json --folder "Scan Operations"

# Export results to various formats
newman run AI-Runtime-Security.postman_collection.json -e your-environment.json --reporters cli,json,html --reporter-json-export results.json
```

## Contributing

Contributions to improve the collection are welcome. Please submit pull requests with any enhancements or bug fixes.

