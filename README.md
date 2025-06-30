# RBZ Exchange Rates API (Developer Documentation)

## Overview
This Laravel package provides access to Zimbabwe's Reserve Bank (RBZ) daily exchange rates by scraping data from their PDF reports.

## Features
- Fetch USD rates specifically
- Fetch all available currency rates
- Automatic PDF parsing and data extraction
- Error handling for missing/invalid data

## Installation
1. Install via Composer:
```bash

 composer require smalot/pdfparser


### Get USD Rate
```bash
curl https://your-api.com/api/rbz-usd-rate

### Get All Currency Rates
```bash
curl https://your-api.com/api/rbz-all-rate
