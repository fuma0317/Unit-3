# Criteria C Development #

Contents
-------------------
1. [Preparation](#preparation)
1. [Login System](#loginsystem)
1. [Registration](#registration)
1. [Database System](#database)


 Preparation:
 ----------
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

 LoginSystem:
 --------------
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
 
**Validation (Showing errors visually)**
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
 if all inputs are valid, it goes to verification method. This method reads email and password hash it. then, open the output.txt file which have all of hashed password. Reads them line by line and checks the password typed by user in login page is there.

 Registration:
 ----------------
**Validation system**
```.py
    def check_register(self):
        email_ok = False
        name_ok = False
        password_ok = False
        confirm_ok = False

        #validation of the input
        email = self.lineEdit_email.text()
        if '@' not in email:
            self.lineEdit_email.setStyleSheet("border: 3px solid orange")

        else:
            self.lineEdit_email.setStyleSheet("border: 3px solid green")
            email_ok = True

        name = self.lineEdit_name.text()
        if name <" ":
            self.lineEdit_name.setStyleSheet("border: 3px solid orange")
        else:
            self.lineEdit_name.setStyleSheet("border: 3px solid green")
            name_ok = True

        password = self.lineEdit_password.text()
        if password <" ":
            self.lineEdit_password.setStyleSheet("border: 3px solid orange")
        else:
            self.lineEdit_password.setStyleSheet("border: 3px solid green")
            password_ok = True

        confirm = self.lineEdit_confirm.text()
        if confirm != password or confirm <" ":
            self.lineEdit_confirm.setStyleSheet("border: 3px solid orange")
        else:
            self.lineEdit_confirm.setStyleSheet("border: 3px solid green")
            confirm_ok = True
        return email_ok, name_ok, password_ok, confirm_ok
 ```
 the text box turns out orange if there is error, if not, it turns out green. It works in the same way as login validation so I won't write an explanation here.
 
 **Storing hashed password in txt file**
 ```.py
     def store(self):
        email = self.lineEdit_email.text()
        password = self.lineEdit_password.text()
        print("Hashing", email + password)
        msg = hash_password(email + password)
        with open('Output.txt', "a") as output_file:
            output_file.write('{}\n'.format(msg))
        self.close()
```
This method reads e-mail and password, then hashes the password with e-mail. And stores it in txt file.

Database:
------------
**Initializer and button connection**
```.py
    def __init__(self, parent=None):
        super(dbofEDM, self).__init__(parent)
        self.setupUi(self)
        self.data = self.load_data()
        self.pushButton_back.clicked.connect(self.goback)
        self.tableWidget.cellChanged.connect(self.changeDB)
        self.pushButton_save.clicked.connect(self.save)
        self.pushButton_revert.clicked.connect(self.cancel)
 ```
 This code is database for EDM musics. So, I have 7 database codes like the one above. I will just explain one of it.
 Also, each buttons and table widget are connected.
 
 **Loading the data inside of csv file**
 ```.py
     def load_data(self):
        # Here we read the comma-separated values file
        data = []
        with open('db_EDM.csv') as EDMdatabase:
            file = csv.reader(EDMdatabase, delimiter=",")
            for i, row in enumerate(file):
                for j, col in enumerate(row):
                    data.append([i, j, col])
                    self.tableWidget.setItem(i, j, QTableWidgetItem(col))
        return data
 ```
 This method opens the csv file and read the data insode of it. Then, shows the data in table widget.
 
 **Editing System for database**
 ```.py
     def changeDB(self):
        item = self.tableWidget.currentItem() #cell clicked
        row = self.tableWidget.currentRow() #row clicked
        col = self.tableWidget.currentColumn() #column clicked
        #change the color of the cell clicked
        self.tableWidget.item(row, col).setBackground(QtGui.QColor(100, 100, 150))
        #show the item in the terminal for debugging purposes
        print(item.text())

        self.pushButton_save.setDisabled(False)
        self.pushButton_revert.setDisabled(False)
 ```
 
