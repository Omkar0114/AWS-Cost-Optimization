# AWS Cost Optimization with Lambda and Python

## Introduction

#### In today's cloud-centric world, managing AWS costs efficiently is essential for organizations to stay competitive and reduce unnecessary expenditures. AWS offers a wide range of tools and services to help optimize costs, but often, it requires a proactive approach to identify and eliminate wasteful resources. This project leverages AWS Lambda, Python, and the Boto3 library to automate cost-saving practices by identifying and deleting unassociated EBS snapshots.

## Getting Started
### Prerequisites
Before you begin, ensure you have met the following requirements:

- AWS account with necessary IAM permissions to create and manage Lambda functions, EC2 instances, and EBS snapshots.
- Python 3.x runtime for lambda function.

## Usage
### Configuration
Before running the Lambda function, you need to configure the AWS credentials and customize the script to suit your environment. Here's how to do it:

AWS Credentials:
1. Sign in to the AWS console and create your account.
2. You're now with the root permissions, it is best practice to create an IAM user and attach policies to specific users. You can read more about it here - https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html

## Step-By-Step Implementation:-
## Create the EC2 instance with volume and snapshot out of it.
- Go to the EC2 instance and create an EC2 instance with the volume as shown below.
![image](https://github.com/Omkar0114/AWS-Cost-Optimization/assets/88308267/ae137d81-f204-42d7-bbd0-796405afc3d2)
![image](https://github.com/Omkar0114/AWS-Cost-Optimization/assets/88308267/a58d35e4-4860-470e-896c-e4796d5fe47a)

- Create a snapshot for EBS volume
![image](https://github.com/Omkar0114/AWS-Cost-Optimization/assets/88308267/fc70321c-adda-4fc7-b7f8-d9eb8ababf3d)
![image](https://github.com/Omkar0114/AWS-Cost-Optimization/assets/88308267/5b24ec19-f7c6-4143-9f67-8410fc44dd49)

- Create a lambda function using python runtime
![image](https://github.com/Omkar0114/AWS-Cost-Optimization/assets/88308267/40c83d4c-5143-4b9e-9d1b-3324add51208)

- Configure the python code in lambda code console. You can find code here - [python_code]()
![image](https://github.com/Omkar0114/AWS-Cost-Optimization/assets/88308267/1281532c-6858-49cc-a005-626c74e4283e)

- Configure the IAM roles and policies for lambda function execute access.
![image](https://github.com/Omkar0114/AWS-Cost-Optimization/assets/88308267/a1897f42-550b-4a3f-a683-bfd37f77c878)

- First Deploy the code and then test. You will see the EBS volume will be Terminated successfully.
![image](https://github.com/Omkar0114/AWS-Cost-Optimization/assets/88308267/be20738e-5db4-45c9-b047-93849620bd97)


## Contributing
### Contributions to this project are welcome! To contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix: `git checkout -b feature/new-feature`
3. Make your changes and commit them: `git commit -m 'Add new feature'`
4. Push to your forked repository: `git push origin feature/new-feature`
5. Create a pull request to merge your changes into the main repository

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.

## Acknowledgments
Mention any libraries, tutorials, or resources that you found helpful during the development of this project.


