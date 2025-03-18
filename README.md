# First Koinos Dapp

A lightweight web application that allows users to check token balances on the Koinos blockchain.

![image](https://github.com/user-attachments/assets/7209b035-69bc-402f-bb13-7b10fb8c34fa)

## Overview

This simple dapp demonstrates how to interact with the Koinos blockchain API to query token balances for any address or nickname. The application features a clean, mobile-friendly interface built with PicoCSS.

## Features

- Check token balances for any Koinos address or nickname
- Support for any token contract on Koinos
- Mobile-friendly, responsive design
- Clean, minimal user interface

## Getting Started

### Prerequisites

- A modern web browser
- Basic understanding of HTML, CSS, and JavaScript

### Running the Application

1. Clone the repository:
   ```
   git clone https://github.com/Open-Koinos/first-dapp.git
   ```

2. Open `index.html` in your web browser.

3. The application will load with default values (@helloworld account and KOIN contract address).

### Usage

1. Enter a Koinos address or nickname (prefixed with @) in the "Address/Nickname" field
2. Enter the token contract address in the "Contract" field
3. Click "Update" to fetch and display the balance

## How It Works

The application uses Axios to make API calls to the Koinos blockchain REST API:

```javascript
axios.get(`https://api.koinos.io/v1/token/${contract}/balance/${wallet}`)
  .then(response => {
    const symbol = contract === '15DJN4a8SgrbGhhGksSBASiSYjGnMU8dGL' ? 'KOIN' : 'tokens';
    balance.textContent = response.data.value + ' ' + symbol;
  })
```

The UI is built using PicoCSS, a minimal CSS framework that provides a clean, responsive design with minimal effort.

## Customization

You can customize this application by:

- Modifying the CSS styles to match your branding
- Adding additional functionality like token transfers
- Integrating with other Koinos blockchain features
- Adding support for multiple token balances display

## Resources

- [Koinos Blockchain](https://koinos.io/)
- [Koinos Documentation](https://docs.koinos.io/)
- [PicoCSS Framework](https://picocss.com/)
