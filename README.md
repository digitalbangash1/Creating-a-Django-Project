# Step-by-Step Guide to Creating a Django Project with the Recommended Folder Structure including good practices
By **Muhammad Bangash**
## Prerequisites

* Python 3.x
* pip

## Instructions



1. We will start with creating a virtual environment in Python for the project so 
all the necessary packages or dependencies can be installed inside the virtual environment
o create a virtual environment in Python for your project, you can follow these steps:

Open your terminal or command prompt.

Navigate to the directory where you want to create your project.

Run the following command to create a new virtual environment:


```python -m venv myenv```

This will create a new virtual environment in a directory named myenv.

Activate the virtual environment by running the following command:

On Windows:

```myenv\Scripts\activate.bat```

On Unix or Linux:

```source myenv/bin/activate```

That's it! You now have a virtual environment set up for your Python project.

2. Install Django by running the following command in your terminal:

```pip install django```

1. Create a new Django project by running the following command in your terminal:

```django-admin startproject project_name```

This will create a new folder named `project_name` in your current directory, which contains the following files:

```
project_name/
├── manage.py
└── project_name/
├── init.py
├── settings.py
├── urls.py
└── wsgi.py
```

`manage.py` is a command-line utility that helps you manage various aspects of your Django project, such as running the
development server, creating database tables, and more.

The `project_name` folder contains the settings and configuration files for your project.

3. Navigate to the `project_name` folder and create a new app by running the following command:

``` python manage.py startapp app_name ```

This will create a new folder named `app_name` inside your project folder, which contains the following files:

```
app_name/
├── init.py
├── admin.py
├── apps.py
├── models.py
├── tests.py
└── views.py

```

`models.py` contains the database models for your app, while `views.py` contains the logic for handling HTTP requests
and generating HTTP responses.

4. (Optional) You can also create additional apps by repeating step 3.

```
python manage.py startapp app_name2
python manage.py startapp app_name3
```

This will create two more app folders with the same file structure as `app_name`.

5. (Optional) If you want to change the default settings for your project, you can modify the `settings.py` file inside
   your project folder.

For example, you can configure the database settings, add middleware, set up static and media file directories, and
more.

That's it! You now have a basic Django project with the recommended folder structure.

6. How to Add an App Name to the `INSTALLED_APPS` List in `settings.py`

To add an app name to the `INSTALLED_APPS` list in your `settings.py` file, follow these steps:

a. Open the `settings.py` file in your project directory using your preferred text editor.

b. Locate the `INSTALLED_APPS` list. It should be near the top of the file.

c. Add the name of your app to the list in quotes, separated by a comma. For example, if your app is named `app_name`,
the line should look like this:

```
INSTALLED_APPS = [
'django.contrib.admin',
'django.contrib.auth',
'django.contrib.contenttypes',
'django.contrib.sessions',
'django.contrib.messages',
'django.contrib.staticfiles',
'app_name', # Add your app name here
]
```

Replace app_name with the actual name of the app you created. Save the settings.py file.

That's it! Django will now recognize your app as part of your project and include it when it runs. You can now start
building your app.













