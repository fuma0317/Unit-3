# Criteria C Development #
### Preparation:
Before coding the system of the inventory application, I needed to develop some basic things as preparation.
Without this prepation, we can't even start this project. So, this is crucial in that sense and this page also could be a memorandum.
**Converting ui file into python file interminal console**
```
pyuic5 Mainpage.ui -o Mainpage.py
```
**Importing class from other python file**
```.py
from register import Register as reg
```
If you have register.py file and class that is called Register inside, you can import the class like the way above. Also, you can rename the class to make it easy to identify. In this cas, I call the class "reg".
**Importing the basis of application**
```.py
from PyQt5 import QtCore, QtGui, QtWidgets
from PyQt5.QtWidgets import QApplication, QMainWindow, QAction, QTableWidgetItem
```
