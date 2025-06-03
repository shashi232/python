# Communication Tools Automation

![Python](https://img.shields.io/badge/Python-3.11%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)

This repository contains Python scripts for automating various communication tasks across different platforms.

## Features

- 📱 WhatsApp message scheduling
- ✉️ Email sending functionality
- 📞 Phone number parsing and validation
- (Coming soon) Text-to-speech capabilities

## Getting Started

### Prerequisites

- Python 3.11+
- Pip package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/communication-tools.git
cd communication-tools
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### WhatsApp Messaging
```python
import pywhatkit
pywhatkit.sendwhatmsg("+919000000000", "Hello from Python!", 12, 30)
```

### Email Sending
```python
import pywhatkit
pywhatkit.send_mail(
    "your_email@gmail.com",
    "your_password",
    "Important Notification",
    "This is an automated message.",
    "recipient@example.com"
)
```

### Phone Number Parsing
```python
import phonenumbers
number = phonenumbers.parse("+919002439467")
print(f"Country Code: {number.country_code} National Number: {number.national_number}")
```

## Configuration

For email functionality, it's recommended to use environment variables for credentials:

1. Create a `.env` file:
```
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_specific_password
```

2. Install python-dotenv:
```bash
pip install python-dotenv
```

3. Modify your code to use environment variables:
```python
from dotenv import load_dotenv
import os

load_dotenv()
email_user = os.getenv('EMAIL_USER')
email_pass = os.getenv('EMAIL_PASS')
```

## Security Notes

⚠️ **Important Security Considerations**:
- Never commit sensitive information like passwords or API keys to version control
- Use app-specific passwords for email services
- Consider using OAuth where possible instead of direct password authentication
- The WhatsApp automation requires your WhatsApp Web session to remain active

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Roadmap

- [ ] Implement text-to-speech capabilities
- [ ] Add error handling and logging
- [ ] Create GUI interface for non-technical users
- [ ] Add unit tests

## Support

For questions or issues, please open an issue in the repository.

