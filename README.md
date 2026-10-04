# AWS Service Catalog for Self-Service Provisioning

## Project Overview

This project demonstrates self-service provisioning of an Amazon Linux EC2 server using AWS Service Catalog and AWS CloudFormation.

The solution allows an approved user to launch a pre-configured EC2 server through AWS Service Catalog instead of creating the infrastructure manually.

## Objective

- Create an AWS Service Catalog portfolio.
- Create a CloudFormation-based product for an Amazon Linux EC2 server.
- Configure a launch constraint using an IAM role.
- Grant access to the required principal.
- Launch the EC2 server through the Service Catalog self-service interface.
- Document and version-control the project using Git and GitHub.

## AWS Services Used

- AWS Service Catalog
- AWS CloudFormation
- Amazon EC2
- AWS IAM

## Project Structure

```text
AWS-Service-Catalog-Self-Service-Provisioning/
│
├── AWSproj_ppt.pptx
├── Cloud formation template/
│   └── yamlfile.yaml
│
├── screenshots/
│   ├── AWS Service Catalog configuration screenshots
│   └── EC2 provisioning screenshots
│
└── README.md
```

## Implementation Process

### 1. Create the CloudFormation Template

A CloudFormation YAML template was created to define the Amazon Linux EC2 server.

The template accepts parameters such as:

- Instance Type
- Key Name

The default instance type used in the project is:

```text
t2.micro
```

### 2. Create the Service Catalog Product

The CloudFormation template was uploaded as an AWS Service Catalog product named:

```text
Self-Service Linux Server
```

Product version:

```text
1.0
```

### 3. Create the Portfolio

A Service Catalog portfolio named:

```text
Student Self-Service Portfolio
```

was created to organize and control access to the product.

### 4. Configure the Launch Constraint

A launch constraint was configured for the product using the IAM role:

```text
LabRole
```

This allows AWS Service Catalog to use the specified IAM role when provisioning the product.

### 5. Grant Portfolio Access

Access to the portfolio was configured for the required principal so that the authorized user could view and launch the product.

### 6. Launch the Product

The product was opened from:

```text
Service Catalog → Products
```

The following values were selected during launch:

```text
Instance Type: t2.micro
Key Name: vockey
```

A provisioned product name was specified as:

```text
Self-Service-Linux-Server
```

The product was then launched successfully.

## Output

The Service Catalog provisioning completed successfully.

The provisioned product was displayed with:

```text
Name: Self-Service-Linux-Server
Status: Available
Product: Self-Service Linux Server
```

This confirms that the Amazon Linux EC2 server was successfully provisioned through AWS Service Catalog and CloudFormation.

## Workflow

```text
CloudFormation YAML
        ↓
Service Catalog Product
        ↓
Student Self-Service Portfolio
        ↓
Launch Constraint
        ↓
Portfolio Access
        ↓
Service Catalog Products
        ↓
Launch Product
        ↓
CloudFormation Provisioning
        ↓
Amazon Linux EC2 Instance
```

## Benefits

- Provides controlled self-service infrastructure provisioning.
- Reduces the need for manual EC2 configuration.
- Uses CloudFormation for repeatable infrastructure deployment.
- Uses IAM-based access control.
- Provides centralized product management through AWS Service Catalog.
- Improves consistency and reduces configuration errors.

## Project Evidence

The `screenshots` folder contains screenshots showing the configuration and successful provisioning process.

The PowerPoint presentation `AWSproj_ppt.pptx` contains the project presentation.

## Conclusion

The project successfully demonstrates how AWS Service Catalog can be used to provide controlled self-service provisioning of an Amazon Linux EC2 server. The infrastructure is defined using CloudFormation, access is controlled using IAM and Service Catalog portfolio settings, and the final EC2 environment is provisioned through the Service Catalog launch workflow.

## GitHub Repository

https://github.com/SANJAY-ELISETTY/AWS-Service-Catalog-Self-Service-Provisioning
