# Flask app example

In first time, we need to create a virtual environment. You have 2 way for that.

## Using virtualenv

Install the package
```
apt install virtualenv
```

Create a virtual environment
```
virtualenv venv
```

## Using Python3-env

Install the package
```
apt install python3-venv
```

Create a virtual envirnment
```
python3 -m venv venv
```

## Use this one
```
. venv/bin/activate or source venv/bin/activate
```

## Leave this one
```
deactivate
```

# Create application file
Now we can create *app.py* file, and to have a basic website, use this configuration
```
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return "<h1>Welcome on your website ! @evanbtc :)</h1>"

if __name__ == '__main__':
	app.run(debug=True)
```

Finally, you can run your application
```
flask run
```

## Create a requirements file
A requirements file is used to store all packages used in the application. If you change the environement of your application you can reinstall all packages with a simple command.
```
pip3 freeze > requirements.txt
```

For reinstall all packages in the new environement
```
pip3 install -r requirements.txt
```

