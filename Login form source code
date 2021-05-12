from tkinter import *
from functools import partial
import mysql.connector

def validateLogin(username, password):
	print("username entered :", username.get())
	print("password entered :", password.get())
	return

con=mysql.connector.connect(host='localhost',user='root',password='root',

                                database='pythontest')

cur=con.cursor()

cur.execute('show databases')

tkWindow = Tk()  
tkWindow.geometry('400x150')  
tkWindow.title('Login Form')

nameLabel = Label(tkWindow, text="Name").grid(row=0, column=0)
name = StringVar()
nameEntry = Entry(tkWindow, textvariable=name).grid(row=0, column=1)

emailLabel = Label(tkWindow, text="Email Id").grid(row=1, column=0)
email = StringVar()
emailEntry = Entry(tkWindow, textvariable=email).grid(row=1, column=1)  

usernameLabel = Label(tkWindow, text="User Name").grid(row=2, column=0)
username = StringVar()
usernameEntry = Entry(tkWindow, textvariable=username).grid(row=2, column=1)  

passwordLabel = Label(tkWindow,text="Password").grid(row=3, column=0)  
password = StringVar()
passwordEntry = Entry(tkWindow, textvariable=password, show='*').grid(row=3, column=1)  

validateLogin = partial(validateLogin, username, password)

loginButton = Button(tkWindow, text="Login", command=validateLogin).grid(row=4, column=0)  

tkWindow.mainloop()
