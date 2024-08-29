# Objective- Created CI/CD Pipelines of web application using Docker, Jenkins and AWS - Application: django-todo

For the project "Created CI/CD Pipelines of a Django web application (django-todo) using Docker, Jenkins, and AWS," here's a detailed explanation of the working process:

1. **Local Testing:** Initially, the Django application was tested locally to ensure proper functionality. This included running the application using `python3 manage.py runserver` on a local system.

2. **EC2 Setup:** An Ubuntu/Linux EC2 instance was created on AWS. The instance was accessed using SSH or EC2 Instance Connect.

3. **Repository Cloning:** The Django application's repository was cloned onto the EC2 instance.

4. **Dependencies Installation:** Required libraries for the Django application were installed on the EC2 instance. The application was run using `python3 manage.py runserver 0.0.0.0/8000` to check its functionality via the public IPv4 address.

5. **Docker Setup:** Docker was installed on the EC2 instance. A Dockerfile was created to containerize the application. The Docker image was built in the correct directory.

6. **Image Execution:** The Docker image was run, and its output was verified before stopping the container. Appropriate inbound rules were configured in the security group to ensure accessibility.

7. **Jenkins Setup:** Jenkins was installed on the EC2 instance. Once installed, Jenkins was set up by selecting the suggested plugins. An agent was created, followed by the creation of a job for the CD pipeline.

8. **Shell Execution in Jenkins:** A build environment was configured in Jenkins where an execution shell script was added to automate the pipeline tasks.

9. **Pipeline Execution:** The pipeline was successfully executed, allowing the application to run. Any future changes to the application can be directly seen through this automated pipeline.

This setup utilizes AWS EC2 for deployment, Docker for containerization, and Jenkins for CI/CD automation. Following the outlined steps ensures smooth operations within the pipeline.
##
This project involves several critical steps and commands beyond the major points listed, such as configuring environment variables, setting up Jenkins credentials, managing Docker permissions, handling security configurations, and fine-tuning deployment scripts, all of which are essential to successfully automate and deploy the Django application via the CI/CD pipeline.
##

A simple todo app built with django

![todo App](https://raw.githubusercontent.com/shreys7/django-todo/develop/staticfiles/todoApp.png)

### Setup

To get this repository, run the following command inside your git enabled terminal

```bash
$ git clone https://github.com/syedgithub12345/DevOps-to-do-application.git
```

You will need django to be installed in you computer to run this app. Head over to https://www.djangoproject.com/download/ for the download guide

Once you have downloaded django, go to the cloned repo directory and run the following command

```bash
$ python manage.py makemigrations
```

This will create all the migrations file (database migrations) required to run this App.

Now, to apply this migrations run the following command

```bash
$ python manage.py migrate
```

One last step and then our todo App will be live. We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user

```bash
$ python manage.py createsuperuser
```

That was pretty simple, right? Now let's make the App live. We just need to start the server now and then we can start using our simple todo App. Start the server by following command

```bash
$ python manage.py runserver
```

Once the server is hosted, head over to http://127.0.0.1:8000/todos for the App.

Cheers and Happy Coding :)
