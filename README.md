# AWS Thought

## Built With
[![AWS](https://img.shields.io/badge/Amazon%20Web%20Services-232F3E.svg?style=for-the-badge&logo=Amazon-Web-Services&logoColor=white)](https://aws.amazon.com/)
[![DynamoDB](https://img.shields.io/badge/Amazon%20DynamoDB-4053D6.svg?style=for-the-badge&logo=Amazon-DynamoDB&logoColor=white)](https://aws.amazon.com/dynamodb/)
[![EC2](https://img.shields.io/badge/Amazon%20EC2-FF9900.svg?style=for-the-badge&logo=Amazon-EC2&logoColor=white)](https://aws.amazon.com/ec2/)
[![S3](https://img.shields.io/badge/Amazon%20S3-569A31.svg?style=for-the-badge&logo=Amazon-S3&logoColor=white)](https://aws.amazon.com/s3/)
[![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)](https://react.dev/)
[![Node.JS](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/en)
[![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)](https://expressjs.com/)

## Project Overview
This project involves setting up and integrating various AWS services to build a full-stack application. It includes creating an AWS account, setting up API endpoints, integrating database calls into the front end, adding image support, and deploying the application to an EC2 instance. The application allows users to view and create thoughts, manage images associated with thoughts, and access the app through a public URL.

## Features
* **Create an AWS Account**: Manage AWS resources and configurations.
* **Set Up API Endpoints**: Create routes for querying and managing thoughts.
* **Integrate Database with Frontend**: Allow users to view, create, and manage thoughts.
* **Add Images**: Upload and view images associated with thoughts.
* **Deploy Application**: Host the application on an EC2 instance for public access.

## Recent Improvements
* **Enhanced State Management**: The homepage now re-renders automatically upon submission of a new "thought", leveraging React's virtual DOM capabilities for a smoother user experience. Previously, users had to manually reload the page to see new submissions.
* **Streamlined User Interface**: The image upload functionality has been integrated into the main submit button, reducing the number of steps required to complete the form. This change simplifies the user experience and makes the application more intuitive to use.

## Screenshots
![Home](client/public/screenshots/aws-thought-home.png)
*The home page where users can view recent thoughts.*

![Profile](client/public/screenshots/aws-thought-profile.png)
*The profile page displaying user information and their submitted thoughts.*

## Installation

### Prerequisites
* Node.js and npm
* AWS CLI
* AWS account

### AWS Configuration
This application uses AWS S3 for image storage. Ensure you have:

1. Created an S3 bucket for the application.
2. Configured your AWS CLI with appropriate credentials.
3. If deploying to EC2, ensure the instance has an IAM role with necessary permissions to access the S3 bucket.

The application will use the AWS SDK's default credential provider chain, eliminating the need for hardcoded access keys.

### Setup
1. **Clone the Repository**
   ```bash
   git clone https://github.com/kyoriku/aws-thought.git 
   cd aws-thought
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Configure Environment Variables**
   Create a `.env` file in the root directory and add your AWS S3 bucket name.
   ```
   AWS_BUCKET_NAME=your-bucket-name
   ```

4. **Run the Application**
   ```bash
   npm start
   ```

## API Endpoints
* **GET /users**: Retrieve all thoughts.
* **GET /users/:userId**: Retrieve thoughts for a specific user.
* **POST /users**: Create a new thought.

## Image Management
* **POST /image-upload**: Upload an image to the S3 bucket.

## Deployment
1. **Create an EC2 Instance**
   Follow AWS documentation to launch an EC2 instance and configure it.

2. **Deploy the Application**
   * SSH into your EC2 instance.
   * Clone the repository and install dependencies.
   * Configure environment variables on the EC2 instance.
   * Start the application.

3. **Access the Application**
   Visit the public URL provided by AWS to access the application.

## Contributing
Feel free to open issues or submit pull requests to improve the application.

## License
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge&logo=mit)](https://opensource.org/licenses/MIT)

This project is licensed under the [MIT](https://opensource.org/licenses/MIT) license - see the LICENSE file for details.

## Questions
If you have any questions, please email devkyoriku@gmail.com.