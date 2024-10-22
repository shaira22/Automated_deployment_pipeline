# Automated-deployment-pipeline

Automated Deployment Pipeline using Jenkins

This repository contains a basic script to set up an automated deployment pipeline for a simple web application using Jenkins.

Prerequisites

A server with Ubuntu installed.

Git installed on the server.

A GitHub repository containing your web application.

Getting Started

1. Clone this repository on your server.

```shell
git clone https://github.com/GitProSolutions/automated-deployment-pipeline.git
```

2. Run the script to set up Jenkins and deploy the web application.

```shell
sudo ./deploy.sh
```
3. Open your web browser and navigate to http://<your_server_ip>:8080. Follow the steps to set up Jenkins and create a new job.

4. In the "Build Triggers" section, select "Poll SCM" and specify a schedule (e.g. H/15 * * * *).

5. In the "Build" section, select "Execute shell" and enter the following command:

```shell
sudo cp -r [YOUR_REPO]/* /var/www/html/ && sudo systemctl restart apache2
```

6. Save the job and build it to test the deployment pipeline.


Customization

You can customize the script based on your specific requirements. For example, you can use a different web server, a different version of Jenkins, or a different Continuous Integration tool like TravisCI, CircleCI, etc.

Contributing

Feel free to contribute to this repository by creating a pull request or reporting an issue.

License

This project is licensed under the MIT License - see the LICENSE file for details.
