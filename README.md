# CREATE AN AWS ACCOUNT, SET UP A ROOT USER AND AN IAM USER

## AIM

To create an Amazon Web Services (AWS) account and configure the AWS root user and an IAM (Identity and Access Management) user.

## PROBLEM STATEMENT

To understand the process of creating an AWS account, configuring the root user, and creating an IAM user with appropriate permissions.

The experiment demonstrates the basic concepts of AWS account management, identity management, and access control. The root user has complete access to all AWS services and resources, whereas IAM users can be assigned specific permissions based on their roles and requirements.

## ALGORITHM

### Step 1: Create an AWS Account

1. Open the AWS Management Console website: https://aws.amazon.com/console/
2. Click on **Create an AWS Account**.
3. Enter a valid email address and an AWS account name.
4. Verify the email address using the verification code.
5. Create a password for the root user.
6. Enter the required contact information and billing details.
7. Complete the account verification process.
8. Select an appropriate support plan and complete the registration.

### Step 2: Sign in as the Root User

1. Open the AWS Management Console.
2. Select the **Root user** sign-in option.
3. Enter the registered email address.
4. Enter the root user's password.
5. Complete the authentication process.
6. Verify that the AWS Management Console is accessible.

### Step 3: Secure the Root User

1. Navigate to the AWS account security settings.
2. Enable Multi-Factor Authentication (MFA) for the root user.
3. Use an authenticator application or another supported MFA method.
4. Verify the MFA configuration.
5. Avoid using the root user for routine AWS operations.

### Step 4: Create an IAM User

1. Navigate to the IAM service in the AWS Management Console.
2. Select **Users** from the navigation panel.
3. Click on **Create user**.
4. Enter a username for the IAM user.
5. Configure the required access options.
6. Assign permissions to the user using an appropriate IAM policy or group.
7. Review the configuration and create the user.
8. Enable MFA for the IAM user if required.

### Step 5: Verify the IAM User

1. Sign out of the root user account.
2. Open the IAM user sign-in page.
3. Enter the AWS account ID or account alias.
4. Enter the IAM username and password.
5. Sign in to the AWS Management Console.
6. Verify that the user can access only the AWS services and resources allowed by the assigned permissions.

## COMMANDS

The AWS account creation and IAM user configuration are primarily performed using the AWS Management Console.

The following AWS CLI commands can also be used to perform the IAM operations.

### 1. Configure AWS CLI

```bash
aws configure
```

This command configures the AWS CLI with the access key, secret access key, default region, and output format.

### 2. Verify the AWS Identity

```bash
aws sts get-caller-identity
```

This command displays the AWS account ID and the ARN of the currently authenticated identity.

### 3. Create an IAM User

```bash
aws iam create-user --user-name LabUser
```

This command creates an IAM user named `LabUser`.

### 4. Create an IAM Group

```bash
aws iam create-group --group-name LabGroup
```

This command creates an IAM group named `LabGroup`.

### 5. Add the IAM User to the Group

```bash
aws iam add-user-to-group --user-name LabUser --group-name LabGroup
```

This command adds the IAM user to the specified group.

### 6. Attach a Read-Only Policy

```bash
aws iam attach-group-policy --group-name LabGroup --policy-arn arn:aws:iam::aws:policy/ReadOnlyAccess
```

This command attaches the AWS-managed `ReadOnlyAccess` policy to the IAM group.

### 7. List IAM Users

```bash
aws iam list-users
```

This command displays the list of IAM users created in the AWS account.

### 8. List IAM Groups

```bash
aws iam list-groups
```

This command displays the list of IAM groups in the AWS account.

### 9. List Users in a Group

```bash
aws iam get-group --group-name LabGroup
```

This command displays the users belonging to the specified IAM group.

### 10. Verify the Assigned Permissions

```bash
aws iam list-attached-group-policies --group-name LabGroup
```

This command displays the policies attached to the IAM group.

**Note:** AWS CLI commands require valid credentials and appropriate IAM permissions. The root user's access keys should not be created or used for routine CLI operations. The `ReadOnlyAccess` policy is used here as an example of permission assignment.

## OUTPUT

### REG NUMBER: 212224040170

### NAME: Levin Paul David![Uploading Screenshot 2026-10-23 085231.png…]()


<img width="1920" height="1200" alt="Screenshot 2026-10-23 090051" src="https://github.com/user-attachments/assets/2e7792a3-26e8-4725-afce-584879fb077a" />

<img width="1920" height="1200" alt="Screenshot 2026-10-23 085308" src="https://github.com/user-attachments/assets/2cfc54bf-ae0e-47c7-bbd0-ecb7c367c287" />

<img width="1920" height="1200" alt="Screenshot 2026-10-23 091458" src="https://github.com/user-attachments/assets/4c30a11b-8d4b-4d85-8b4e-1315ba214f93" />

<img width="1920" height="1200" alt="Screenshot 2026-10-23 091704" src="https://github.com/user-attachments/assets/a1b7d65e-ca78-4794-bda2-7e5407b3a8fb" />

<img width="1920" height="1200" alt="Screenshot 2026-10-23 083223" src="https://github.com/user-attachments/assets/fed9d47a-59d1-4c83-a737-666c9c60aa69" />

<img width="1920" height="1200" alt="Screenshot 2026-10-23 083641" src="https://github.com/user-attachments/assets/c906f413-8fa1-4b36-82a4-c6f558fcf98d" />

<img width="1920" height="1200" alt="Screenshot 2026-10-23 083756" src="https://github.com/user-attachments/assets/35799fb1-4fdb-4147-8585-7c7a7e83b341" />

<img width="1920" height="1200" alt="Screenshot 2026-10-23 084031" src="https://github.com/user-attachments/assets/4812c5c0-99c9-4d01-9cd3-0fdfc6e7056b" />

<img width="1920" height="1200" alt="Screenshot 2026-10-23 084618" src="https://github.com/user-attachments/assets/c9e0b6d6-6f5e-4b70-ba74-f69c9588d569" />

### OBSERVATION

1. An AWS account was successfully created.
2. The root user was configured and secured using Multi-Factor Authentication.
3. An IAM user was created with the required permissions.
4. The IAM user was successfully authenticated.
5. The assigned permissions were verified using the AWS Management Console and AWS CLI.

## RESULT

Thus, an AWS account was successfully created, the root user was configured and secured, and an IAM user was created with appropriate permissions. The experiment demonstrated the basic concepts of AWS account management, IAM user creation, authentication, and access control.
