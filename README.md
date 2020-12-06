# Invoice-Billing-Management

Clone this repository into the directory of your choice like so:

$ git clone https://github.com/koushikdeva/Invoice-Billing-Management.git

cd into the project root directory and install the needed requirements.
NB: Ensure that your virtual environment is activated.

$ cd Invoice-Management-System/
$ pip install -r requirements.txt

You will need to set the following environment variables. Open your .bashrc file

$ vim ~/.bashrc

and add the following

export SECRET_KEY='{secure secret key}'
export NAME='{database name}'
export USER='{user}'
export PASSWORD='{user password}'
export HOST='{database host ip}'
export PORT='{database port}'

Setup the database by running the following.

$ python manage.py migrate

When all is okay, you can start the local development server.

$ python manage.py runserver

Visit localhost:8000 in your browser.
