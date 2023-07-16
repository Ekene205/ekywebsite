Description: This script automates the installation and setup of the Apache HTTP Server (httpd) on a CentOS-based system. It also downloads a specific website from a GitHub repository and deploys it to the server's web root directory.

Prerequisites
A CentOS-based system (e.g., CentOS 7, CentOS 8)
Internet connectivity
Installation
Follow these steps to use the script:

Clone or download the repository to your local machine.
Open a terminal or command prompt.
Navigate to the directory where the script is located.
Usage
Open the script file using a text editor.
Replace the placeholder URL (https://github.com/Ekene205/ekywebsite/archive/refs/heads/main.zip) with the actual URL of your website's ZIP file on GitHub.
Save the changes.
To run the script, execute the following command:

bash
Copy code
./script.sh
The script will perform the following actions:

Update the system packages by executing yum update -y.
Install necessary dependencies by executing yum install -y.
Install Apache HTTP Server (httpd) by executing yum install -y httpd.
Change the directory to /var/www/html by executing cd /var/www/html.
Download the website ZIP file from the specified GitHub repository by executing wget https://github.com/Ekene205/ekywebsite/archive/refs/heads/main.zip.
Extract the contents of the ZIP file by executing unzip main.zip.
Copy the contents of the extracted folder to the web root directory by executing cp -r ekywebsite-main/* /var/www/html/.
Remove the temporary files and folders by executing rm -rf ekywebsite-main main.zip.
Enable the httpd service to start on boot by executing systemctl enable httpd.
Start the httpd service immediately by executing systemctl start httpd.
Please note that the script assumes that the system has the necessary permissions and prerequisites to execute the provided commands. Make sure you have sufficient privileges before running the script.

Contributing
Contributions are welcome! If you find any issues with the script or have suggestions for improvements, please open an issue or submit a pull request on the GitHub repository.
