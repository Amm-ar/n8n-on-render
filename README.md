# n8n on Render

This repository contains the necessary configuration to deploy [n8n](https://n8n.io/) on Render with a persistent PostgreSQL database.

## Deployment Instructions

1. Click the "Deploy to Render" button below:

   [![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)

2. If you're not already logged in to Render, you'll be prompted to do so.

3. Review the services that will be created:
   - A web service for n8n
   - A PostgreSQL database for persistent data storage

4. Click "Apply" to start the deployment process.

5. Wait for the deployment to complete. This may take a few minutes.

## Accessing the n8n Dashboard

Once deployment is complete:

1. Navigate to your Render dashboard: https://dashboard.render.com/
2. Find your newly created web service (named "n8n" by default)
3. Click on the service to view its details
4. Click on the URL provided in the service details to access your n8n instance
5. You'll be prompted for a username and password:
   - Username: `admin`
   - Password: `changeme`

## Changing the Default Password

For security reasons, you should change the default password immediately after first login:

1. Log in to your n8n dashboard using the default credentials
2. Once logged in, click on the user icon in the top right corner
3. Select "Settings" from the dropdown menu
4. In the "Personal Access Tokens" section, you can change your password
5. Enter your new password in the "New Password" and "Confirm New Password" fields
6. Click "Save" to update your password

Alternatively, you can change the password by updating the environment variables in your Render dashboard:

1. Go to your Render dashboard
2. Click on your n8n web service
3. Click on "Environment" in the sidebar
4. Find the `N8N_BASIC_AUTH_PASSWORD` variable
5. Click the "Edit" button next to it
6. Update the value to your desired password
7. Click "Save Changes"
8. Redeploy your service for the changes to take effect

## Configuration Details

This deployment uses basic authentication with the following default settings:
- Username: `admin`
- Password: `changeme`

The configuration also includes:
- Persistent PostgreSQL database storage
- Auto-generated encryption key for securing credentials

For more information about n8n configuration options, refer to the [n8n documentation](https://docs.n8n.io/).