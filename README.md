# InTouch Core Services Postman Collections

Welcome to the private GitHub repository for the InTouch Core Services Postman Collections. These collections are designed to streamline the process of interacting with InTouch Core Services, enabling developers to initiate workflows, monitor their progress, and access results efficiently.

## Collection Overview

This repository contains two main collections:

- **Workflows Collection**: This collection includes API calls for initiating various workflows, tracking their progress, and retrieving results. It supports a wide range of operations, from consumer trace workflows to KYC and credit checks, providing a structured approach to executing these tasks.

- **Environment Variables Collection**: This collection specifies the necessary environment variables for the Workflows Collection, detailing base URLs, authentication parameters, and other configurations critical for the successful execution of API calls.

## Getting Started

Before utilizing these collections, ensure Postman is installed on your machine. Follow these steps to set up:

1. **Import Collections**: Download the `Workflows Collection` JSON file. In Postman, navigate to `Import` > `File` > `Upload Files` and select the file.

2. **Import Environment Variables**: Download the `Environment Variables Collection` JSON file and import it into Postman using the same method.

3. **Configure Environment**: Choose the imported environment from Postman's top-right environment dropdown. Verify that all variables, especially `base_url`, `auth_url`, `identity_url`, and `injection_url`, are correctly set for your scenario.

## Key Features

### Workflow Initiation and Tracking

- **Initiation Calls**: Using your Organisation ID, you can initiate any workflow process. These calls generate a `Tracking ID`, which is essential for monitoring the workflow's progress.

- **Status Checks**: By inputting the `Tracking ID` as a path variable in the status call, you can obtain real-time updates on the workflow. This includes results for each step as they are completed.

- **Handling Encoded Data**: If a call returns encoded data, the workflow will decode this data and upload the corresponding document or image to a private S3 bucket. You'll receive a document or image URL in your results, equipped with a secure, pre-signed link for access. Note that these links expire after 24 hours for security purposes.

### Environment Variables Collection

This collection includes crucial configurations, such as:

- **Base URLs**: URLs for authentication, identity services, core services, and workflow initiation.
- **Authentication Token**: Placeholder for the Bearer token necessary for authenticated calls.
- **Organisation Phase Two ID**: Identifier used in initiating workflows.

## Usage Guidelines

Please replace placeholders in each request with actual values relevant to your use case. This includes setting appropriate environment variables and ensuring payloads are correctly formatted.

### Initiating a Workflow

Select the corresponding request from the collection, ensure your environment variables are configured, and execute the request. You will receive a `Tracking ID` in response.

### Checking Workflow Status

Use the `Check Workflow Status` request with your `Tracking ID` to monitor the current status of your initiated workflow.

## Security and Privacy Notice

Given the sensitive nature of the information and operations within this repository, please exercise utmost caution to avoid exposing authentication tokens, personal identifiers, or any sensitive data.

## License

The contents of this repository are provided under a private license. Unauthorized distribution, sharing, or copying of any content without explicit permission is strictly prohibited.

## Support

Should you require assistance or further information, please do not hesitate to contact [support@intouch.io](mailto:support@intouch.io).
