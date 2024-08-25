# Decentralized Supply Chain Management DApp

## Overview

This DApp is a decentralized supply chain management system built using Cartesi. It tracks products through various stages of the supply chain, providing transparency and immutability.

## Features

- **Product Creation**: Create new product entries with details.
- **Update Product Status**: Update the status of products as they progress through the supply chain.
- **Inspect Product Status**: View the current status and history of products.

## Getting Started

### Prerequisites

- Node.js and npm installed.
- Cartesi Rollups server URL.

### Installation

1. **Clone the Repository**

   ```bash
   git clone <repository_url>
   cd <repository_directory>
   ```

2. **Install Dependencies**

   ```bash
   npm install
   ```

3. **Set Up Environment Variables**

   Create a `.env` file in the root directory and add the following environment variables:

   ```env
   ROLLUP_HTTP_SERVER_URL=<your_rollup_server_url>
   ```

4. **Run the Application**

   Start the application by running:

   ```bash
   node index.js
   ```

## Usage

### Creating a Product

Send a request to create a new product with the following JSON payload:

```json
{
  "action": "create",
  "productId": "product1",
  "details": {
    "name": "Product One",
    "status": "Manufacturing"
  }
}
```

### Updating Product Status

Send a request to update the status of an existing product with the following JSON payload:

```json
{
  "action": "update",
  "productId": "product1",
  "details": {
    "status": "Shipped"
  }
}
```

### Inspecting Products

Send a request to inspect the status of all products with the following JSON payload:

```json
{
  "payload": "products"
}
```

## File Structure

- `index.js`: Main file for handling requests and managing product state.
- `.env`: Environment variables configuration file.