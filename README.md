# Lambda Code for AWS Cloud Resume Challenge

This repository contains the Python code for an AWS Lambda function used in the Cloud Resume Challenge. The function is set up to automatically update via GitHub Actions whenever changes are pushed to the repository.

## Features

- **Automatic Deployment**: GitHub Actions are configured to automatically update the AWS Lambda function upon any push to the repo.
- **Visitor Counter**: This Lambda function updates a DynamoDB table that tracks the number of visitors to a website.

## Setup

### Prerequisites

- AWS account with permissions to create and update Lambda functions.
- AWS CLI configured with your credentials.
- GitHub repository linked to your AWS Lambda function.

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/amanuelararso/lambda-code-for-AWS-CRC.git
   cd lambda-code-for-AWS-CRC
   ```

2. **Set up GitHub Secrets:**
   - `AWS_ACCESS_KEY_ID`
   - `AWS_SECRET_ACCESS_KEY`
   - `AWS_REGION`
   - `LAMBDA_FUNCTION_NAME`

3. **Configure GitHub Actions:**
   The workflow file (`.github/workflows/deploy.yml`) is already set up to deploy the Lambda function automatically.

## Usage

1. **Make changes to the Python code (`lambda_function.py`):**
   Modify the `lambda_function.py` file as needed.

2. **Push changes to the repository:**
   ```bash
   git add .
   git commit -m "Update Lambda function"
   git push origin main
   ```

3. **Automatic Deployment:**
   GitHub Actions will trigger and update your AWS Lambda function with the latest code.

## Dependencies

- `boto3`: AWS SDK for Python.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Contact

For any questions or issues, please open an issue in this repository.
