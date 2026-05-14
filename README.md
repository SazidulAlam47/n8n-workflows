# n8n Messenger Bot Workflows

This repository contains two exported n8n workflows for Facebook Messenger automation:

- Bistro Boss Messenger Bot.json
- VeyronixBd Messenger Bot.json

Both workflows use an n8n AI Agent with Messenger-style conversational flows, memory, and external tools to support customer interactions.

## Workflows

### Bistro Boss Messenger Bot

This workflow is a restaurant support bot for Bistro Boss, a restaurant in Dhanmondi, Dhaka. It is designed to handle Facebook Messenger conversations for:

- menu inquiries
- food ordering
- table reservations for special events
- customer support around delivery, dine-in, and booking questions

Main integrations and behavior:

- Facebook Messenger webhook for receiving messages and sending replies
- n8n AI Agent for human-like conversation handling
- live menu lookup from a website REST API
- food order creation through a backend payment/order API
- table availability lookup and reservation flow
- simple session memory to keep conversation context

The workflow is configured to respond in the same language style the customer uses, including English, Bengali, and Banglish.

### VeyronixBd Messenger Bot

This workflow is a sales and support bot for Veyronix BD, an e-commerce brand focused on gadgets and lifestyle products. It is designed to handle Facebook Messenger conversations for:

- product questions
- product price checks
- order collection
- order submission to Google Sheets

Main integrations and behavior:

- Facebook Messenger webhook for receiving messages and sending replies
- n8n AI Agent for customer conversation handling
- Google Sheets lookup for product data
- Google Sheets append operation for order storage
- simple session memory to keep conversation context

The workflow asks for customer details such as name, phone number, email, delivery address, quantity, and payment method before adding an order to the sheet.

## Repository Structure

- Bistro Boss Messenger Bot.json: restaurant bot workflow export
- VeyronixBd Messenger Bot.json: e-commerce bot workflow export

## Notes

- These files are n8n workflow exports, so they can be imported into n8n directly.
- The workflow JSON includes live integrations and configuration values that should be reviewed before reuse.
- If you plan to deploy these workflows in a new environment, verify webhook URLs, API credentials, and spreadsheet connections first.

## Summary

In short, this repo is a small collection of production-style n8n Messenger automations:

- one for restaurant ordering and reservations
- one for product support and order capture through Google Sheets
