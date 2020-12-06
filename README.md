# Invoice Management System

## Setup

### Using Python virtualenv

#### Prerequisites
* You have a working installation of Python 2.7.*
* You can install software on your system.
* You can create and activate Python virtual environments.
Create a Python virtual environment somewhere on your system and activate it.
Your shell prompt should look something like this:
```shell
(env)[username@computer pwd]$
```

Clone this repository into the directory of your choice like so:
```shell
$ git clone https://github.com/koushikdeva/Invoice-Billing-Management.git
```

`cd` into the project root directory and install the needed requirements.  
NB: Ensure that your virtual environment is activated.
```shell
$ cd Invoice-Management-System/
$ pip install -r requirements.txt
```

You will need to set the following environment variables. 
Open your .bashrc file
```shell
$ vim ~/.bashrc
```

and add the following 
```shell
export SECRET_KEY='{secure secret key}'
export NAME='{database name}'
export USER='{user}'
export PASSWORD='{user password}'
export HOST='{database host ip}'
export PORT='{database port}'
```

Setup the database by running the following.
```shell
$ python manage.py migrate
```


### Running
When all is okay, you can start the local development server.
```shell
$ python manage.py runserver
```

Visit `localhost:8000` in your browser.


## Features

## Testing
Run the commands below to test the project and view the coverage.
```shell
$ coverage run --source='.' manage.py test
$ coverage report -m
```
To exclude the virtualenv folder do the following:
```shell
$ coverage run --omit ve  --source="." manage.py  test
```
In the above example "ve" is the name of the virtualenv.
