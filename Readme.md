#The instruction to setup a virtual environment

We usually work on different projects with different libraries,
even with different versions of same libraries. Therefore, we should 
use virtual environments. <br>
Each project works on a specific virtual environment. 

Set execute permission to *setup.sh*, then run it
```commandline
chmod +x setup.sh
./setup.sh
```


Add the below lines to ~/.profile
```
# virtualenv and virtualenvwrapper
export WORKON_HOME=$HOME/.virtualenvs
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
source /usr/local/bin/virtualenvwrapper.sh
```

similarly, add these lines to ~/.bashrc
```
export WORKON_HOME=~/.virtualenvs
VIRTUALENVWRAPPER_PYTHON='/usr/bin/python3'
source /usr/local/bin/virtualenvwrapper.sh
```
Execute these commands:
```commandline
source ~/.profile
source ~/.bashrc
```

Now, we're going to create a virtual environment:
```
mkvirtualenv imrc -p python3
```
(__*imrc*__ is the name of your environment)

To work on the new environment, execute the command:
```commandline
workon imrc
```

Now, you are in the virtual environment named *imrc*, you should
install essential libraries in the environment for our work.
The libraries are listed in the *requirement.txt* file, you can 
modify (add/delete) libraries that you don't need to use. <br>
Obviously, you can install any libraries whenever you want.
Run the command to install libraries listed in the *requirement.txt*:
 ```commandline
pip install -r requirement.txt
```

Now, you can work with the essential libs.
To check the libraries that are installed in your environment, run:
```commandline
pip list
```

Thank you.