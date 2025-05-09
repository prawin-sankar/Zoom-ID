# Zoom-ID
Create a Zoom ID with pro access request

# Zoom Pro Access Request Automation

This repository contains an automated system for handling Zoom Pro access requests within an organization. The system streamlines the process of requesting, approving, and provisioning Zoom Pro licenses.

## Features

- **Automated Request Processing**: Streamlined workflow for submitting Zoom Pro access requests
- **Integration with AWS Bedrock**: AI-powered request analysis and approval recommendations
- **Ticket Management**: Automated ticket creation and tracking
- **Approval Workflow**: Multi-level approval process with automated notifications
- **License Provisioning**: Automated Zoom license assignment upon approval

## System Architecture

### Components

1. **Frontend Interface**
   - Streamlit-based chatbot interface
   - User-friendly request submission form
   - Real-time request status tracking

2. **Backend Services**
   - AWS Bedrock Agent for request processing
   - FastAPI-based ticket management system
   - GitHub Actions for workflow automation

3. **Integration Points**
   - Zoom Admin API integration
   - Email notification system
   - Jira/ServiceNow integration (optional)

## Setup Instructions

### Prerequisites

- Python 3.11 or higher
- AWS Account with Bedrock access
- Zoom Admin API credentials
- GitHub account

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/zoom-pro-access-request.git
   cd zoom-pro-access-request
   ```

2. Create and activate virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Configure environment variables:
   ```bash
   cp .env.example .env
   # Edit .env with your credentials
   ```

### Configuration

1. **AWS Bedrock Setup**
   - Configure AWS credentials
   - Set up Bedrock Agent with appropriate permissions
   - Configure knowledge base for request processing

2. **Zoom API Setup**
   - Generate Zoom Admin API credentials
   - Configure API scopes for license management
   - Set up webhook endpoints

3. **GitHub Actions Setup**
   - Configure repository secrets
   - Set up workflow permissions
   - Configure branch protection rules

## Usage

### Submitting a Request

1. Access the Streamlit interface:
   ```bash
   streamlit run app.py
   ```

2. Fill out the request form with:
   - Employee details
   - Department information
   - Justification for Zoom Pro access
   - Required features

3. Submit the request through the chatbot interface

### Request Processing

1. **Initial Review**
   - AWS Bedrock analyzes the request
   - Generates approval recommendations
   - Creates a ticket in the system

2. **Approval Workflow**
   - Manager approval
   - IT department review
   - Final approval

3. **License Provisioning**
   - Automated Zoom license assignment
   - Email notification to user
   - Access details provided

## Development

### Project Structure

```
zoom-pro-access-request/
├── app.py                 # Streamlit application
├── api/                   # FastAPI backend
├── scripts/              # Utility scripts
├── .github/workflows/    # GitHub Actions
└── tests/               # Test suite
```

### Adding New Features

1. Create a new branch:
   ```bash
   git checkout -b feature/new-feature
   ```

2. Implement changes
3. Add tests
4. Submit pull request

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Security

- All API keys and credentials are stored as environment variables
- HTTPS encryption for all communications
- Regular security audits
- Access logging and monitoring

## Support

For support, please:
1. Check the documentation
2. Open an issue in the repository
3. Contact the IT support team

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- AWS Bedrock team
- Zoom API team
- Contributors and maintainers 
