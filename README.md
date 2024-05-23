
# Notification

The Notification API is a JavaScript library that allows you to send and manage notifications within your web application. This README provides an overview of the API, its installation, usage, and examples.

## Table of Contents

1. Installation
2. Usage
3. API Reference
- initialize
- sendNotification
- requestPermission
- getPermissionStatus
4. Examples
5. Contributing
6. License

## Installation

You can install the Notification API using npm:

```bash
npm install notification-api
```

Or include it directly in your HTML file:

```html
<script src="path/to/notification-api.js"></script>
```

## Usage

First, you need to initialize the Notification API and request permission to send notifications:

```javascript
import { initialize, requestPermission } from 'notification-api';

// Initialize the API
initialize();

// Request permission to send notifications
requestPermission().then(permission => {
    if (permission === 'granted') {
        console.log('Notification permission granted.');
    } else {
        console.log('Notification permission denied.');
    }
});
```
To send a notification, use the sendNotification function:

```javascript
import { sendNotification } from 'notification-api';

sendNotification('Hello!', {
    body: 'This is a test notification.',
    icon: 'path/to/icon.png'
});
```

## Contributing

We welcome contributions! Please read our contributing guidelines to get started.

## License

This project is licensed under the MIT License - see the LICENSE file for details.