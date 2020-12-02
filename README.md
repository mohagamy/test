
Pillow
Matplotlib 
Numpy
OpenCV 
Requests
Keras
TensorFlow
Theano
NLTK (Natural Language Toolkit)
Fire
Arrow
FlashText
Scipy 
SQLAlchemy
wxPython
PyTorch
BeautifulSoup 
Bokeh
Pandas 
Scikit Learn
subprocess
NetworkX 
osBrain


## remove python2

```shell
whereis python
which python

# Remove python2
sudo apt purge -y python2.7-minimal
sudo apt autoremove

# You already have Python3 but 
# don't care about the version 
sudo ln -s /usr/bin/python3 /usr/bin/python

# Same for pip
sudo apt install -y python3-pip
sudo ln -s /usr/bin/pip3 /usr/bin/pip

# Confirm the new version of Python: 3
python --version
```

