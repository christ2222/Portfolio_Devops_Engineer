

# Portfolio Project

Welcome to my Portfolio Project repository! This project showcases my skills and experience in setting up a static website using AWS services, including a 2-stage CI/CD pipeline.

## Project Overview

This project demonstrates the deployment of a static website using the following AWS services:

- **S3 Bucket**: To store and host the static files.
- **GitHub**: As the version control system.
- **AWS CodePipeline**: To automate the CI/CD pipeline.
- **CloudFront**: For content delivery.
- **Route 53**: For DNS management.
- **AWS Certificate Manager (ACM)**: For SSL/TLS certificate management.

## Architecture

See attached portfolio.diagram.png

### Services Breakdown

- **Amazon S3**: Stores the static website files (HTML, CSS, JavaScript).
- **AWS CodePipeline**: Orchestrates the CI/CD pipeline, which includes:
  - **Source Stage**: Retrieves the source code from GitHub.
  - **Deploy Stage**: Deploys the built files to the S3 bucket.
- **Amazon CloudFront**: Distributes the website content globally with low latency.
- **Amazon Route 53**: Manages the DNS records for the domain.
- **AWS Certificate Manager (ACM)**: Manages the SSL/TLS certificates for secure connections.

## CI/CD Pipeline

The CI/CD pipeline consists of two stages:

1. **Staging**: 
   - Deploys the latest code changes to a staging environment.
   - Allows for testing and verification before production deployment.
2. **Production**: 
   - Deploys the verified changes from the staging environment to the production environment.

## Setup Instructions

### Prerequisites

- An AWS account with necessary permissions.
- A registered domain name.
- Basic knowledge of AWS services and GitHub.

### Steps to Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/portfolio-project.git
   cd portfolio-project
   ```

2. **Create an S3 bucket**:
   - Log in to the AWS Management Console.
   - Navigate to S3 and create a new bucket (e.g., `your-portfolio-bucket`).

3. **Set up AWS CodePipeline**:
   - Create a new pipeline in AWS CodePipeline.
   - Set the source provider to GitHub and connect your repository.
   - Add a deploy stage to deploy to the S3 bucket.

4. **Configure CloudFront**:
   - Create a CloudFront distribution.
   - Set the origin to the S3 bucket.
   - Configure the necessary settings for caching and distribution.

5. **Set up Route 53**:
   - Create a hosted zone for your domain.
   - Add a record set for your CloudFront distribution.

6. **Request an SSL/TLS certificate with ACM**:
   - Use ACM to request a public certificate for your domain.
   - Validate the certificate with DNS validation.

7. **Deploy the website**:
   - Commit and push your changes to GitHub.
   - AWS CodePipeline will automatically trigger the pipeline and deploy the website.

## Usage
- **Production Environment**: Accessible at `myportfolio.logotse.com`.

## Contributing

Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to modify this template to better fit your project specifics!
