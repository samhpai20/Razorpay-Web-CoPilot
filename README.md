# Razorpay Integration Co-Pilot

A comprehensive integration assistant that helps developers implement Razorpay payment gateway into their applications across multiple programming languages.

## 🚀 Features

- **Multi-language Support**: PHP, JavaScript/Node.js, Python, Ruby, Go, and .NET
- **Complete Integration Workflow**: From account setup to production deployment
- **Security Best Practices**: Signature verification, webhook validation, and more
- **Comprehensive Test Suites**: Ensure your integration works flawlessly
- **Production-Ready Code**: Use in real applications with minimal modifications

## 📋 Table of Contents

- [Installation](#installation)
- [Quick Start](#quick-start)
- [Languages Supported](#languages-supported)
- [Integration Steps](#integration-steps)
- [Testing](#testing)
- [Security Considerations](#security-considerations)
- [Contributing](#contributing)
- [License](#license)

## 🔧 Installation

```bash
# Using npm
npm install razorpay-copilot

# Using yarn
yarn add razorpay-copilot
```

## 🏃‍♂️ Quick Start

```javascript
// Import the co-pilot
const RazorpayCopilot = require('razorpay-copilot');

// Create a new instance
const razorpayCopilot = new RazorpayCopilot();

// Set your preferred language
razorpayCopilot.setLanguage('php'); // Options: 'php', 'javascript', 'node.js', 'python', 'ruby', 'go', '.net'

// Configure your API keys
razorpayCopilot.setCredentials('rzp_test_your_key_id', 'your_key_secret', 'your_webhook_secret');

// Get checkout integration code
razorpayCopilot.goToStep(razorpayCopilot.steps.INTEGRATE_CHECKOUT);
const checkoutCode = razorpayCopilot.getCurrentStepGuidance();
console.log(checkoutCode);
```

## 🌐 Languages Supported

| Language | Extensions | Frameworks Supported |
|----------|------------|----------------------|
| JavaScript | .js | Vanilla JS, Node.js, Express, React, Next.js |
| PHP | .php | Core PHP, Laravel, CodeIgniter, Symfony |
| Python | .py | Flask, Django, FastAPI |
| Ruby | .rb | Rails, Sinatra |
| Go | .go | Standard library, Gin, Echo |
| .NET | .cs | ASP.NET Core, MVC |

## 🛣️ Integration Steps

The co-pilot guides you through these key integration steps:

1. **Account Setup**: Create and configure your Razorpay merchant account
2. **API Keys**: Securely manage your API credentials
3. **Checkout Integration**: Add the payment form to your application
4. **Payment Handling**: Process successful and failed payments
5. **Signature Verification**: Validate payment signatures for security
6. **Webhook Setup**: Configure notifications for payment events
7. **Testing**: Comprehensive testing with Razorpay test credentials
8. **Go Live**: Transition from test to production environment

### Detailed Usage

```javascript
// Move through integration steps
razorpayCopilot.nextStep(); // Move to next step
razorpayCopilot.previousStep(); // Move to previous step

// Jump to a specific step
razorpayCopilot.goToStep(razorpayCopilot.steps.VERIFY_SIGNATURE);

// Get guidance for current step
const currentStepGuidance = razorpayCopilot.getCurrentStepGuidance();

// Toggle between test and live modes
razorpayCopilot.setMode('test'); // Use 'test' during development, 'live' for production
```

## 🧪 Testing

The co-pilot provides test suites for all supported languages. Access them with:

```javascript
razorpayCopilot.goToStep(razorpayCopilot.steps.RUN_TEST_SUITE);
const testSuite = razorpayCopilot.getCurrentStepGuidance();
```

### Test Cards

| Card Network | Card Number | CVV | Expiry Date |
|--------------|-------------|-----|-------------|
| Visa | 4111 1111 1111 1111 | Any 3 digits | Any future date |
| Mastercard | 5267 3181 8797 5449 | Any 3 digits | Any future date |
| RuPay | 6062 8205 0180 0900 | Any 3 digits | Any future date |

### International Test Cards

| Card Network | Card Number | CVV | Expiry Date |
|--------------|-------------|-----|-------------|
| Visa | 4012 8888 8888 1881 | Any 3 digits | Any future date |
| Mastercard | 5104 0600 0000 0008 | Any 3 digits | Any future date |

### Other Test Methods

- **UPI**: `success@razorpay` (for successful payments), `failure@razorpay` (for failed payments)
- **Netbanking**: Any bank with account number `1111111`
- **Wallet**: Any wallet with phone number `77777 77777`

## 🔒 Security Considerations

- Never store API keys in client-side code
- Always verify payment signatures for all transactions
- Use environment variables for storing sensitive credentials
- Use HTTPS for all API communications
- Implement proper error handling and logging
- Validate all webhook requests using the webhook secret
- Follow PCI-DSS compliance guidelines when handling payment data

## 👨‍💻 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Setup

```bash
# Clone the repository
git clone https://github.com/your-username/razorpay-copilot.git

# Install dependencies
cd razorpay-copilot
npm install

# Run tests
npm test
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

```
MIT License

Copyright (c) 2025 Razorpay Co-Pilot

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 🙏 Acknowledgements

- [Razorpay Documentation](https://razorpay.com/docs)
- All contributors who have helped shape this project
- Open source libraries used in the development of this tool

## 📊 Usage Examples

### PHP Example

```php
<?php
// Include the co-pilot
require 'vendor/autoload.php';

use RazorpayCopilot\RazorpayCopilot;

// Create a new instance
$razorpayCopilot = new RazorpayCopilot();
$razorpayCopilot->setLanguage('php');
$razorpayCopilot->setCredentials('rzp_test_your_key_id', 'your_key_secret');

// Get signature verification code
$razorpayCopilot->goToStep($razorpayCopilot->steps['VERIFY_SIGNATURE']);
$verificationCode = $razorpayCopilot->getCurrentStepGuidance();

// Output the code
echo $verificationCode;
?>
```

### Python Example

```python
# Import the co-pilot
from razorpay_copilot import RazorpayCopilot

# Create a new instance
copilot = RazorpayCopilot()
copilot.set_language('python')
copilot.set_credentials('rzp_test_your_key_id', 'your_key_secret')

# Get webhook handling code
copilot.go_to_step(copilot.steps.SETUP_WEBHOOK)
webhook_code = copilot.get_current_step_guidance()

# Print the code
print(webhook_code)
```

---

⭐️ If this tool helped you, please consider giving it a star on GitHub! ⭐️
