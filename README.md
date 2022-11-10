# Rootoo-Network
Dapshen Studios \ Rootoo Network [Versions 1.0-2.0]

_______________________________________________________________________________________________________________________________________________________________________

Version 1.0

from turtle import*
from random import*

speed(0)
ids = 0
t1 = Turtle()
t2 = Turtle()
t1.shape("square")
t2.shape("square")
t1.penup()
t2.penup()
t2.left(90)
t2.forward(50)
t2.right(90)
t1.write('    войти', font=('Arial', 14, 'normal'))
t2.write('    создать', font=('Arial', 14, 'normal'))
accounts = {}
login = 'id'
def logup(x,y):
    global ids
    accounts[ids] = randint(100000, 999999)
    print(ids,accounts[ids])
    ids = ids + 1
def login(x,y):
    login = int(input("Введите ID: "))
    password = int(input("Введите пароль: "))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login)
    else:
        print('Вы не вошли в аккаунт', login)
t1.onclick(login)
t2.onclick(logup)
mainloop()

_______________________________________________________________________________________________________________________________________________________________________

Version 1.1

from turtle import*
from random import*
speed(0)
ids = 0
t1 = Turtle()
t2 = Turtle()
t1.shape("square")
t2.shape("square")
t1.penup()
t2.penup()
t2.left(90)
t2.forward(50)
t2.right(90)
t1.write('    войти', font=('Arial', 14, 'normal'))
t2.write('    создать', font=('Arial', 14, 'normal'))
accounts = {}
balance = {}
login = 'id'
def logup(x,y):
    global ids
    accounts[ids] = randint(100000, 999999)
    print(ids,accounts[ids])
    balance[ids] = 0
    balance[ids] = balance[ids] + 1
    ids = ids + 1
def login(x,y):
    login = int(input("Введите ID: "))
    password = int(input("Введите пароль: "))
    if accounts[login] == password:
        print("Вы вошли в аккаунт", login,"/", balance[login])
    else:
        print("Вы не вошли в аккаунт")

t1.onclick(login)
t2.onclick(logup)
mainloop()

_______________________________________________________________________________________________________________________________________________________________________

Version 1.2

from turtle import*
from random import*
speed(0)
ids = 0
t1 = Turtle()
t2 = Turtle()
t3 = Turtle()
t1.shape("square")
t2.shape("square")
t3.shape("square")
t1.penup()
t2.penup()
t3.penup()
t2.left(90)
t2.forward(50)
t2.right(90)
t3.left(90)
t3.forward(100)
t3.right(90)
t1.write('    войти', font=('Arial', 14, 'normal'))
t2.write('    создать', font=('Arial', 14, 'normal'))
t3.write('    отправить', font=('Arial', 14, 'normal'))
accounts = {}
balance = {}
login = 'id'
def logup(x,y):
    global ids
    accounts[ids] = randint(100000, 999999)
    print(ids,accounts[ids])
    balance[ids] = 1
    ids = ids + 1
def login(x,y):
    login = int(input("Введите ID: "))
    password = int(input("Введите пароль: "))
    if accounts[login] == password:
        print("Вы вошли в аккаунт", login,"/",balance[login],"ROOTOO")
    else:
        print("Вы не вошли в аккаунт")
def send(x,y):
    login = int(input("Введите ID: "))
    password = int(input("Введите пароль: "))
    if accounts[login] == password:
        print("Вы вошли в аккаунт", login,"/",balance[login],"ROOTOO","отправление ROOTOO")
        amount = int(input("сумма отправления: "))
        if amount <= balance[login]:
            deposit = int(input("адрес получателя"))
            balance[login] = balance[login] - amount
            balance[deposit] = balance[deposit] + amount
            print("перевод успешно завершён!!! отправления с кошелька: ",login,"на кошелёк: ",deposit,amount,"/","ROOTOO")
        else:
            print("Извините но на вашем балансе не достатачно средств.")
    else:
        print("Вы не вошли в аккаунт")

t1.onclick(login)
t2.onclick(logup)
t3.onclick(send)
mainloop()

_______________________________________________________________________________________________________________________________________________________________________

Version 1.3

from turtle import*
from random import*
speed(0)
ids = 0
t1 = Turtle()
t2 = Turtle()
t3 = Turtle()
t4 = Turtle()
t1.shape("square")
t2.shape("square")
t3.shape("square")
t4.shape("square")
t1.penup()
t2.penup()
t3.penup()
t4.penup()
t2.left(90)
t2.forward(50)
t2.right(90)
t3.left(90)
t3.forward(100)
t3.right(90)
t4.left(90)
t4.forward(150)
t4.right(90)
t1.write('    войти', font=('Arial', 14, 'normal'))
t2.write('    создать', font=('Arial', 14, 'normal'))
t3.write('    отправить', font=('Arial', 14, 'normal'))
t4.write('    Rootoo Scan', font=('Arial', 14, 'normal'))
accounts = {}
balance = {}
login = 'id'
sending = (":send ")
end = (" >>")
blockchain = [balance]
def logup(x,y):
    global ids
    accounts[ids] = randint(100000, 999999)
    print(ids,accounts[ids])
    balance[ids] = 1
    ids = ids + 1
def login(x,y):
    login = int(input("Введите ID: "))
    password = int(input("Введите пароль: "))
    if accounts[login] == password:
        print("Вы вошли в аккаунт", login,"/",balance[login],"ROOTOO")
    else:
        print("Вы не вошли в аккаунт")
def send(x,y):
    global blockchain
    global sending
    global end
    login = int(input("Введите ID: "))
    password = int(input("Введите пароль: "))
    if accounts[login] == password:
        print("Вы вошли в аккаунт", login,"/",balance[login],"ROOTOO","отправление ROOTOO")
        amount = int(input("сумма отправления: "))
        if amount <= balance[login]:
            deposit = int(input("адрес получателя"))
            balance[login] = balance[login] - amount
            balance[deposit] = balance[deposit] + amount
            print("перевод успешно завершён!!! отправления с кошелька: ",login,"на кошелёк: ",deposit,"в сумме:",amount,"ROOTOO")
            blockchain = (blockchain,sending,login,deposit,amount,end)
        else:
            print("Извините но на вашем балансе не достатачно средств.")
    else:
        print("Вы не вошли в аккаунт")
def rootooscan(x,y):
    global blockchain
    print(blockchain)
t1.onclick(login)
t2.onclick(logup)
t3.onclick(send)
t4.onclick(rootooscan)
mainloop()

_______________________________________________________________________________________________________________________________________________________________________

Version 1.4
