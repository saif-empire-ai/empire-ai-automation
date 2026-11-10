# EMPIRE Pharma WhatsApp AI Agent — Setup Guide

## Overview

This project provides an n8n workflow example for pharmaceutical WhatsApp automation, including product inquiries, message routing, medicine image analysis, and order-processing logic.

This is a demonstration project, not a production-ready medical or ordering system.

## Requirements

- An n8n instance with compatible workflow nodes
- A WhatsApp Business API provider such as ChakraHQ
- A Google account with Google Sheets access
- An OpenAI API account for image analysis
- Test data containing fictional pharmaceutical products

API usage and third-party services may incur charges.

## Installation

1. Download `empire-pharma-whatsapp-github-safe.json` from this repository.
2. Open your n8n dashboard.
3. Create a new workflow.
4. Import the downloaded JSON file.
5. Keep the workflow inactive while configuring integrations.
6. Inspect all nodes for missing credentials, placeholders, and compatibility warnings.

## Google Sheets Configuration

1. Create a Google Sheets document for demo pharmaceutical products.
2. Create a sheet named `pharma_products`.
3. Add the columns required by the imported workflow.
4. Add fictional test products.
5. Configure your own Google Sheets credentials securely in n8n.
6. Replace `REPLACE_WITH_YOUR_GOOGLE_SHEET_ID` with your document ID.

Check the workflow's field mappings before running it.

## ChakraHQ / WhatsApp Configuration

1. Configure a WhatsApp Business API account with your provider.
2. Set up the required webhook integration.
3. Replace placeholder provider identifiers and endpoints where applicable.
4. Store API tokens in n8n credentials instead of hardcoding secrets in nodes.
5. Configure the HTTP Request nodes for your provider's API.
6. Test only with authorized test phone numbers.

Do not commit live API tokens, customer phone numbers, or private webhook secrets.

## OpenAI Image Analysis

1. Configure an OpenAI credential in n8n.
2. Open the Analyze Medicine Image node.
3. Select a supported model.
4. Verify that the incoming image binary property matches the node configuration.
5. Test with a non-sensitive sample medicine package image.

AI-generated medicine information may be incorrect. Verify product identity and medical information independently. Do not use this demo for clinical decisions.

## Testing

- Confirm text messages route to the correct branch.
- Confirm image messages route to the image-processing branch.
- Check Google Sheets lookup and product-field mappings.
- Test order validation with fictional data.
- Inspect errors and execution logs.
- Confirm that no private information is stored in test outputs.

## Security

- Never publish real API credentials or access tokens.
- Remove customer and patient information.
- Use fictional test data.
- Review workflow exports before sharing.
- Rotate any previously exposed credentials.
- Apply appropriate access controls and data-protection measures before production use.

## Current Status

Public demonstration workflow. Importability has been checked, but end-to-end functionality and production security have not been independently verified.

## License

MIT License — see the LICENSE file.

## Maintainer

Md Saif Ahmad  
AI Automation Developer & Founder  
Empire AI Automation Solution
