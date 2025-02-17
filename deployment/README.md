# Deployment README 
## Setting Up Environment Variables for Database Password 
Before deploying the application, ensure that the following environment variable is set to configure the database password securely: 
- **DB_PASSWORD**: This variable should contain the password for the database connection. 
### Steps to Set Environment Variable 
1. **For Local Deployment:** 
   - On Unix/Linux/MacOS, you can set the environment variable in the terminal before starting the application: 
     ```sh 
     export DB_PASSWORD=your_secure_password 
     ``` 
   - On Windows, use the command prompt: 
     ```cmd 
     set DB_PASSWORD=your_secure_password 
     ``` 
2. **For Cloud Deployment:** 
   - Refer to your cloud provider's documentation for setting environment variables. For example: 
     - **AWS Elastic Beanstalk**: Navigate to the "Configuration" section, select "Software" and add the environment variable under "Environment properties". 
     - **Heroku**: Use the Heroku CLI to set the config variable: 
       ```sh 
       heroku config:set DB_PASSWORD=your_secure_password 
       ``` 
3. **For Docker Deployment:** 
   - Modify your Docker run command or Docker Compose file to include the environment variable: 
     ```sh 
     docker run -e DB_PASSWORD=your_secure_password your_image_name 
     ``` 
By ensuring that these steps are included in your deployment process, you will have securely externalized the database password configuration, enhancing the security of your application. 