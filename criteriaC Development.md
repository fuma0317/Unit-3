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

### Login System:
I began to create the codes for login system as a first step as it is the first window that users would deal with.

**Creating initializer**
```.py
class loginPage(log):
    def __init__(self, parent=None):
        super(loginPage, self).__init__(parent)
        self.setupUi(self)
```
**Creating a system to connect the buttons with each methods**
```.py
        self.pushButton_login.clicked.connect(self.try_login)
        # This is a behaviour for the quit button
        self.pushButton_quit.clicked.connect(self.quitApp)
        self.pushButton_register.clicked.connect(self.regApp)
 ```
 This should be included in the initializer. This part enables to connect to methods if the particular button is clicked.
 
 **Creating exit system**
 ```.py
  def quitApp(self):
        sys.exit(0) #0 means exit without errors
 ```
 **Showing registration app if tthe button is clicked**
 ```.py
 #This opens the registration form
    def regApp(self):
        regVar = register(self)
        regVar.show()
```
This method is connected to the button in initializer.
 
