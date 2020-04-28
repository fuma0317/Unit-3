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
 **Showing registration app if the button is clicked**
 ```.py
 #This opens the registration form
    def regApp(self):
        regVar = register(self)
        regVar.show()
```
This method is connected to the button by the part in initializer.
 
**Showing errors visually**
```.py
    def check_login(self):

        #validation of the input
        email_ok = False
        password_ok = False
        email = self.lineEdit.text()
        if email < " ":
            self.lineEdit.setStyleSheet("border: 3px solid orange")
        else:
            self.lineEdit.setStyleSheet("border: 3px solid green")
            email_ok = True

        password = self.lineEdit_2.text()
        if password < " ":
            self.lineEdit_2.setStyleSheet("border: 3px solid orange")
        else:
            self.lineEdit_2.setStyleSheet("border: 3px solid green")
            password_ok = True

        return email_ok, password_ok
 ```
text box turns into orange as error in the case which nothing is in text box or '@' is not included in e-mail text box or confirm is not same as password. If they are all okay, it turns into green

**Creating verification system**
```.py
    def try_login(self):
        if self.check_login():
            self.verification()

    def verification(self):
        email = self.lineEdit.text()
        password = self.lineEdit_2.text()
        with open('Output.txt', mode='rt') as f:
            for user in f:
                cph = verify_password(user, email + password)
                if cph == True:
                    self.done(0)
 ```
