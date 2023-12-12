[[ Back to All Guidelines ]](../readme.md)


# Backend Guidelines

## 1. Setting Up Your Local Development Environment

### 1.1 Operating System
- Ubuntu (Recommended)
- Windows with WSL

### 1.2 Python Version
- Python 3.8

### 1.3 Editor
- VS Code
- PyCharm (Recommended)

### 1.4 Project Setup
1. Fork the project.
2. Run [Script](https://nagarro.sharepoint.com/:u:/s/CrowdBoticsTeam/EXHr9JHjLxNGrA9u2hfNMQIBJWGiDoBP4bAlFe7r1UKzxw?e=EXPeRw) for cloning and running the project locally including docker and database setup.
3. Verify all the initial settings of the project like unique identifier in user table as it may cause issue to alter this after the initial migration.
4. Deploy the application on the CB dashboard.
5. Setup the staging environment.
6. Create separate branch for staging and map the same to staging environment.

## 2. Best Practices
1. Always try to make use of crowdbotics modules as much as possible.
2. Always maintain third party API keys and URL in the environment variable so that they can easily be changed from the dashboard page based on the environment.
3. Try to follow modular approach and create the separate app for each functionality.
4. Implement API security carefully and make sure that authorized person can access the data and only the authorized data is visible to user.

## 3. Functionalities Related Setup Documents

### 3.1 Background Jobs (Celery)
Please refer this [document](https://nagarro.sharepoint.com/:t:/s/CrowdBoticsTeam/ERF-1xon-jBCk9A5W6js9awBPeudnmiM_YmLRKuFLpB_PA?e=5afea6) for celery setup.

### 3.2 In-App Subscriptions
(Provide setup details for In-App Subscriptions)

## 4. Recommended Libraries / Packages
1. django-filter
