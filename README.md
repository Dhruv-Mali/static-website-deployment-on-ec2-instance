# static-website-deployment-on-ec2-instance

Deploying a static website on an AWS EC2 instance involves several steps. Here's a high-level step-by-step process:

1. **Create an AWS EC2 Instance:**
   - Log in to your AWS account.
   - Navigate to the EC2 dashboard.
   - Launch a new EC2 instance with the desired OS (e.g., Amazon Linux, Ubuntu).

2. **SSH into your EC2 Instance:**
   - Use an SSH client to connect to your EC2 instance.

3. **Update and Install Software:**
   - Update the package lists on your instance: `sudo apt update` (for Ubuntu) or `sudo yum update` (for Amazon Linux).
   - Install a web server (e.g., Apache or Nginx) if not already installed: `sudo apt install apache2` (for Apache) or `sudo yum install nginx` (for Nginx).

4. **Upload Your Website Files:**
   - Use SCP, SFTP, or other methods to transfer your static website files to the EC2 instance. You can use the `scp` command for this.

5. **Configure the Web Server:**
   - For Apache, you'll need to configure the virtual host to point to your website's directory. Edit the virtual host configuration file, usually found in `/etc/apache2/sites-available/`, and restart Apache.
   - For Nginx, create a server block configuration in `/etc/nginx/sites-available/` and link it to `/etc/nginx/sites-enabled/`. Don't forget to remove the default configuration if needed. Then, restart Nginx.

6. **Set Up Domain Name (Optional):**
   - If you have a domain name, you can configure it to point to your EC2 instance's public IP by updating DNS records.

7. **Secure Your Website with SSL (Optional):**
   - You can use Let's Encrypt to get a free SSL certificate for your website, especially if you're using Nginx or Apache. Follow their instructions for your specific web server.

8. **Configure Security Groups:**
   - Make sure your EC2 instance's security group allows HTTP (port 80) and HTTPS (port 443) traffic.

9. **Test Your Website:**
   - Open a web browser and enter your EC2 instance's public IP or domain name to verify that your website is accessible.

10. **Back Up Your Website:**
   - Consider setting up regular backups of your website and EC2 instance to prevent data loss.

Remember that these are general steps, and the exact commands and configurations can vary depending on the specific Linux distribution you're using, the web server software, and other factors. Always refer to AWS and the documentation of the software you're using for the most up-to-date instructions.



this is my project to deploy static websites http://54.163.16.26/
