# CrossClassify API

## Introduction

The CrossClassify API provides services for making and retrieving decisions related to fraud detection. This API is designed to help integrate fraud detection capabilities into your applications. Access to the API requires an `x-api-key` and `auth token`, which can be obtained from the project's settings at [app.crossclassify.com](https://app.crossclassify.com).

## Table of Contents

- [Getting started](#getting-started)
- [Configuration](#configuration)
- [Usage](#usage)
  - [Making a New Decision](#making-a-new-decision)
  - [Retrieving a Decision](#retrieving-a-decision)
- [Dependencies](#dependencies)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)
- [License](#license)

## Getting started

Before you can use the CrossClassify API, ensure that your environment is set up correctly and that you have the necessary authentication credentials:

1. Obtain your API key and authentication token from your project settings on CrossClassify's application page.
2. Configure your HTTP client to include these credentials in the headers of your requests.

## Configuration

- **API Base URL:** `https://api.crossclassify.com/v1/`
- **Authentication:** Use the API key and token for accessing the endpoints. The API key should be included in the request header as `X-API-Key`.

## Usage

### Making a New Decision

**Endpoint:** `/projects/{projectId}/fraudServices/{serviceName}/newDecision`

**Method:** POST

**Description:** Initiates the process of making a new decision for a specified service within a project.

**Request Body:**
- Required: Yes
- Content-Type: `application/json`
- Fields: Detailed in the schema definitions for `newDecision_post`.

**Success Response:**
- Code: 201
- Content: Information about the decision process initiation.

**Error Response:**
- Code: Corresponding HTTP error code
- Content: Error description and details

### Retrieving a Decision

**Endpoint:** `/projects/{projectId}/fraudServices/{serviceName}/newDecision/{newDecisionId}`

**Method:** GET

**Description:** Retrieves the details of a previously requested decision.

**Success Response:**
- Code: 200
- Content: Details of the decision.

**Error Response:**
- Code: Corresponding HTTP error code
- Content: Error description and details

## Dependencies

This API requires the following dependencies:
- HTTP client for making API requests.
- JSON parser for handling response data.

## Troubleshooting

If you have any issues , contact us at [support@crossclassify.com](support@crossclassify.com).

