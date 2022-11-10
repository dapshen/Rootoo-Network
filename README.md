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

from turtle import*
from random import*
speed(0)
ids = 0
sites = 0
t1 = Turtle()
t2 = Turtle()
t3 = Turtle()
t4 = Turtle()
t5 = Turtle()
t1.shape("square")
t2.shape("square")
t3.shape("square")
t4.shape("square")
t5.shape("square")
t1.penup()
t2.penup()
t3.penup()
t4.penup()
t5.penup()
t2.left(90)
t2.forward(50)
t2.right(90)
t3.left(90)
t3.forward(100)
t3.right(90)
t4.left(90)
t4.forward(150)
t4.right(90)
t5.left(90)
t5.forward(200)
t5.right(90)
t1.write('    войти', font=('Arial', 14, 'normal'))
t2.write('    создать', font=('Arial', 14, 'normal'))
t3.write('    отправить', font=('Arial', 14, 'normal'))
t4.write('    Rootoo Scan', font=('Arial', 14, 'normal'))
t5.write('    Denet Browser', font=('Arial', 14, 'normal'))
accounts = {}
balance = {}
denet_hranilishe = {}
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
def denet(x,y):
    global sites
    vibor = input("Что сделать? создать новый denet ?- тогда напиши -denet- / если просто поиск - то нажми -ENTER- ")
    if vibor == "denet":
        k1 = input("пишите код denet сайта: ")
        denet_hranilishe[sites] = k1
        print("Адрес вашего сайта: ", sites)
        sites = sites + 1
    else:
        poisk = int(input("Введите ссылку на denet: "))
        print("Вы зашли на denet: ", poisk)
        print(denet_hranilishe[poisk])
t1.onclick(login)
t2.onclick(logup)
t3.onclick(send)
t4.onclick(rootooscan)
t5.onclick(denet)
mainloop()

_______________________________________________________________________________________________________________________________________________________________________

Version 1.5

from turtle import*
from random import*
from time import*
speed(0)
ids = 0
sites = 0
froze = "Froze and Stake for 100 Seconds"
t1 = Turtle()
t2 = Turtle()
t3 = Turtle()
t4 = Turtle()
t5 = Turtle()
t6 = Turtle()
t1.shape("square")
t2.shape("square")
t3.shape("square")
t4.shape("square")
t5.shape("square")
t6.shape("square")
t1.penup()
t2.penup()
t3.penup()
t4.penup()
t5.penup()
t6.penup()
t2.left(90)
t2.forward(50)
t2.right(90)
t3.left(90)
t3.forward(100)
t3.right(90)
t4.left(90)
t4.forward(150)
t4.right(90)
t5.left(90)
t5.forward(200)
t5.right(90)
t6.left(90)
t6.forward(250)
t6.right(90)
t1.write('    войти', font=('Arial', 14, 'normal'))
t2.write('    создать', font=('Arial', 14, 'normal'))
t3.write('    отправить', font=('Arial', 14, 'normal'))
t4.write('    Rootoo Scan', font=('Arial', 14, 'normal'))
t5.write('    Denet Browser', font=('Arial', 14, 'normal'))
t6.write('    Froze and Stake', font=('Arial', 14, 'normal'))
accounts = {}
balance = {}
denet_hranilishe = {}
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

def denet(x,y):
    global sites
    vibor = input("Что сделать? создать новый denet ?- тогда напиши -denet- / если просто поиск - то нажми -ENTER- ")
    if vibor == "denet":
        k1 = input("пишите код denet сайта: ")
        denet_hranilishe[sites] = k1
        print("Адрес вашего сайта: ", sites)
        sites = sites + 1
    else:
        poisk = int(input("Введите ссылку на denet: "))
        print("Вы зашли на denet: ", poisk)
        print(denet_hranilishe[poisk])

def froze(x,y):
    global blockchain
    global froze
    global end
    login = int(input("Введите ID: "))
    password = int(input("Введите пароль: "))
    if accounts[login] == password:
        print("Вы вошли в аккаунт", login,"/",balance[login],"ROOTOO","Заморозка + стэйкинг")
        amount = int(input("сумма заморозки: "))
        if amount <= balance[login]:
            balance[login] = balance[login] - amount
            print("ЗАМОРОЗКА УСПЕШНО ЗАВЕРШЕНА!!! заморозка с кошелька: ",login,"в сумме:",amount,"ROOTOO")
            blockchain = (blockchain,froze,login,amount,end)
            profit = amount/10
            sleep(100)
            balance[login] = balance[login] + amount + profit
        else:
            print("Извините но на вашем балансе не достатачно средств.")
    else:
        print("Вы не вошли в аккаунт")

t1.onclick(login)
t2.onclick(logup)
t3.onclick(send)
t4.onclick(rootooscan)
t5.onclick(denet)
t6.onclick(froze)
mainloop()

_______________________________________________________________________________________________________________________________________________________________________

Version 1.6

from turtle import*
from random import*
from time import*
speed(0)
ids = 0
sites = 0
froze = 'Froze and Stake for 100 Seconds'
t1 = Turtle()
t2 = Turtle()
t3 = Turtle()
t4 = Turtle()
t5 = Turtle()
t6 = Turtle()
t1.shape('square')
t2.shape('square')
t3.shape('square')
t4.shape('square')
t5.shape('square')
t6.shape('square')
t1.penup()
t2.penup()
t3.penup()
t4.penup()
t5.penup()
t6.penup()
t2.left(90)
t2.forward(50)
t2.right(90)
t3.left(90)
t3.forward(100)
t3.right(90)
t4.left(90)
t4.forward(150)
t4.right(90)
t5.left(90)
t5.forward(200)
t5.right(90)
t6.left(90)
t6.forward(250)
t6.right(90)
t1.write('    войти', font=('Arial', 14, 'normal'))
t2.write('    создать', font=('Arial', 14, 'normal'))
t3.write('    отправить', font=('Arial', 14, 'normal'))
t4.write('    Rootoo Scan', font=('Arial', 14, 'normal'))
t5.write('    Denet Browser', font=('Arial', 14, 'normal'))
t6.write('    Froze and Stake', font=('Arial', 14, 'normal'))
accounts = {}
balance = {}
denet_hranilishe = {}
login = 'id'
sending = (':send ')
end = (' >>')
blockchain = [balance]
def logup(x,y):
    global ids
    accounts[ids] = randint(100000, 999999)
    print(ids,accounts[ids])
    balance[ids] = 1
    ids = ids + 1
def login(x,y):
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO')
    else:
        print('Вы не вошли в аккаунт')
def send(x,y):
    global blockchain
    global sending
    global end
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO','отправление ROOTOO')
        amount = int(input('сумма отправления: '))
        if amount <= balance[login]:
            deposit = int(input('адрес получателя'))
            balance[login] = balance[login] - amount
            balance[deposit] = balance[deposit] + amount
            print('перевод успешно завершён!!! отправления с кошелька: ',login,'на кошелёк: ',deposit,'в сумме:',amount,'ROOTOO')
            blockchain = (blockchain,sending,login,deposit,amount,end)
        else:
            print('Извините но на вашем балансе не достатачно средств.')
    else:
        print('Вы не вошли в аккаунт')

def rootooscan(x,y):
    global blockchain
    print(blockchain)

def denet(x,y):
    global sites
    vibor = input('Что сделать? создать новый denet ?- тогда напиши -denet- / если просто поиск - то нажми -ENTER- ')
    if vibor == "denet":
        k1 = input('пишите код denet сайта: ')
        denet_hranilishe[sites] = k1
        print('Адрес вашего сайта: ', sites)
        sites = sites + 1
    else:
        poisk = int(input('Введите ссылку на denet: '))
        print('Вы зашли на denet: ', poisk)
        print(denet_hranilishe[poisk])

def froze(x,y):
    global blockchain
    global froze
    global end
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO','Заморозка + стэйкинг')
        amount = int(input('сумма заморозки: '))
        if amount <= balance[login]:
            balance[login] = balance[login] - amount
            print('ЗАМОРОЗКА УСПЕШНО ЗАВЕРШЕНА!!! заморозка с кошелька: ',login,'в сумме:',amount,'ROOTOO')
            blockchain = (blockchain,froze,login,amount,end)
            profit = amount/10
            sleep(100)
            balance[login] = balance[login] + amount + profit
        else:
            print('Извините но на вашем балансе не достатачно средств.')
    else:
        print('Вы не вошли в аккаунт')

t1.onclick(login)
t2.onclick(logup)
t3.onclick(send)
t4.onclick(rootooscan)
t5.onclick(denet)
t6.onclick(froze)
mainloop()

_______________________________________________________________________________________________________________________________________________________________________

Version 1.7

from turtle import*
from random import*
from time import*
speed(0)
ids = 0
sites = 0
froze = 'Froze and Stake for 100 Seconds'
t1 = Turtle()
t2 = Turtle()
t3 = Turtle()
t4 = Turtle()
t5 = Turtle()
t6 = Turtle()
t7 = Turtle()
t1.shape('square')
t2.shape('square')
t3.shape('square')
t4.shape('square')
t5.shape('square')
t6.shape('square')
t7.shape('square')
t1.penup()
t2.penup()
t3.penup()
t4.penup()
t5.penup()
t6.penup()
t7.penup()
t2.left(90)
t2.forward(50)
t2.right(90)
t3.left(90)
t3.forward(100)
t3.right(90)
t4.left(90)
t4.forward(150)
t4.right(90)
t5.left(90)
t5.forward(200)
t5.right(90)

t6.right(90)
t6.forward(50)
t6.left(90)
t7.right(90)
t7.forward(100)
t7.left(90)

t1.write('    войти', font=('Arial', 14, 'normal'))
t2.write('    создать', font=('Arial', 14, 'normal'))
t3.write('    отправить', font=('Arial', 14, 'normal'))
t4.write('    Rootoo Scan', font=('Arial', 14, 'normal'))
t5.write('    Denet Browser', font=('Arial', 14, 'normal'))
t6.write('    Froze and Stake', font=('Arial', 14, 'normal'))
t7.write('    Поменять Пароль', font=('Arial', 14, 'normal'))
accounts = {}
balance = {}
denet_hranilishe = {}
login = 'id'
sending = (':send ')
end = (' >>')
blockchain = [balance]
def logup(x,y):
    global ids
    accounts[ids] = randint(100000, 999999)
    print(ids,accounts[ids])
    balance[ids] = 1
    ids = ids + 1
def login(x,y):
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO')
    else:
        print('Вы не вошли в аккаунт')
def send(x,y):
    global blockchain
    global sending
    global end
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO','отправление ROOTOO')
        amount = int(input('сумма отправления: '))
        if amount <= balance[login]:
            deposit = int(input('адрес получателя'))
            balance[login] = balance[login] - amount
            balance[deposit] = balance[deposit] + amount
            print('перевод успешно завершён!!! отправления с кошелька: ',login,'на кошелёк: ',deposit,'в сумме:',amount,'ROOTOO')
            blockchain = (blockchain,sending,login,deposit,amount,end)
        else:
            print('Извините но на вашем балансе не достатачно средств.')
    else:
        print('Вы не вошли в аккаунт')

def rootooscan(x,y):
    global blockchain
    print(blockchain)

def denet(x,y):
    global sites
    vibor = input('Что сделать? создать новый denet ?- тогда напиши -denet- / если просто поиск - то нажми -ENTER- ')
    if vibor == "denet":
        k1 = input('пишите код denet сайта: ')
        denet_hranilishe[sites] = k1
        print('Адрес вашего сайта: ', sites)
        sites = sites + 1
    else:
        poisk = int(input('Введите ссылку на denet: '))
        print('Вы зашли на denet: ', poisk)
        print(denet_hranilishe[poisk])

def froze(x,y):
    global blockchain
    global froze
    global end
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO','Заморозка + стэйкинг')
        amount = int(input('сумма заморозки: '))
        if amount <= balance[login]:
            balance[login] = balance[login] - amount
            print('ЗАМОРОЗКА УСПЕШНО ЗАВЕРШЕНА!!! заморозка с кошелька: ',login,'в сумме:',amount,'ROOTOO')
            blockchain = (blockchain,froze,login,amount,end)
            profit = amount/10
            sleep(100)
            balance[login] = balance[login] + amount + profit
        else:
            print('Извините но на вашем балансе не достатачно средств.')
    else:
        print('Вы не вошли в аккаунт')

def change_password(x,y):
    
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт, меняйте пароль', login,'/',balance[login],'ROOTOO')
        new_password = int(input('введите новый пароль -): '))
        print('Ваш новый пароль:', new_password)
        sleep(1)
        print('ОБРАБОТКА...')
        sleep(1)
        accounts[login] = new_password
        print('Пароль успешно изменён!!!')
    else:
        print('Вы ввели неправильный логин/пароль')
        


t1.onclick(login)
t2.onclick(logup)
t3.onclick(send)
t4.onclick(rootooscan)
t5.onclick(denet)
t6.onclick(froze)
t7.onclick(change_password)
mainloop()

_______________________________________________________________________________________________________________________________________________________________________

Version 1.8

from turtle import*
from random import*
from time import*
speed(0)
ids = 0
sites = 0
froze = 'Froze and Stake for 100 Seconds'
t1 = Turtle()
t2 = Turtle()
t3 = Turtle()
t4 = Turtle()
t5 = Turtle()
t6 = Turtle()
t7 = Turtle()
t1.shape('square')
t2.shape('square')
t3.shape('square')
t4.shape('square')
t5.shape('square')
t6.shape('square')
t7.shape('square')
t1.penup()
t2.penup()
t3.penup()
t4.penup()
t5.penup()
t6.penup()
t7.penup()
t2.left(90)
t2.forward(50)
t2.right(90)
t3.left(90)
t3.forward(100)
t3.right(90)
t4.left(90)
t4.forward(150)
t4.right(90)
t5.left(90)
t5.forward(200)
t5.right(90)

t6.right(90)
t6.forward(50)
t6.left(90)
t7.right(90)
t7.forward(100)
t7.left(90)

t1.write('    войти', font=('Arial', 14, 'normal'))
t2.write('    создать', font=('Arial', 14, 'normal'))
t3.write('    отправить', font=('Arial', 14, 'normal'))
t4.write('    Rootoo Scan', font=('Arial', 14, 'normal'))
t5.write('    Denet Browser', font=('Arial', 14, 'normal'))
t6.write('    Froze and Stake', font=('Arial', 14, 'normal'))
t7.write('    Поменять Пароль', font=('Arial', 14, 'normal'))
accounts = {}
balance = {}
denet_hranilishe = {}
login = 'id'
sending = (':send ')
end = (' >>')
blockchain = [balance]
nomer = 0
otpravitel = {}
poluchatel = {}
summa = {}
def logup(x,y):
    global ids
    accounts[ids] = randint(100000, 999999)
    print(ids,accounts[ids])
    balance[ids] = 1
    ids = ids + 1
def login(x,y):
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO')
    else:
        print('Вы не вошли в аккаунт')
def send(x,y):
    global blockchain
    global sending
    global end
    global otpravitel
    global poluchatel
    global summa
    global nomer
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO','отправление ROOTOO')
        amount = int(input('сумма отправления: '))
        if amount <= balance[login]:
            deposit = int(input('адрес получателя'))
            balance[login] = balance[login] - amount
            balance[deposit] = balance[deposit] + amount
            print('перевод успешно завершён!!! отправления с кошелька: ',login,'на кошелёк: ',deposit,'в сумме:',amount,'ROOTOO')
            otpravitel[nomer] = login
            poluchatel[nomer] = deposit
            summa[nomer] = amount
            blockchain = (blockchain,nomer,sending,login,deposit,amount,end)
            print('номер транзакции:', nomer)
            otpravitel[nomer] = login
            poluchatel[nomer] = deposit
            summa[nomer] = amount
            nomer = nomer + 1
        else:
            print('Извините но на вашем балансе не достатачно средств.')
    else:
        print('Вы не вошли в аккаунт')

def rootooscan(x,y):
    global blockchain
    vibor = input('напишите цифру действия для выполнения \n 1 - просмотр транзакции по номеру \n 2 - посмотреть баланс пользователя по адресу \n 3 - посмотреть весь блокчейн: ')
    if vibor == '1':
        tranza = int(input('введите номер транзакции: '))
        print('с адреса')
        print(otpravitel[tranza])
        print('на адрес')
        print(poluchatel[tranza])
        print('сумма отправления')
        print(summa[tranza])
    elif vibor == '2':
        adress = int(input('Введите адрес пользователя: '))
        print(blockchain[adress])
    elif vibor == '3':
        print(blockchain)
def denet(x,y):
    global sites
    vibor = input('Что сделать? создать новый denet ?- тогда напиши -denet- / если просто поиск - то нажми -ENTER- ')
    if vibor == "denet":
        k1 = input('пишите код denet сайта: ')
        denet_hranilishe[sites] = k1
        print('Адрес вашего сайта: ', sites)
        sites = sites + 1
    else:
        poisk = int(input('Введите ссылку на denet: '))
        print('Вы зашли на denet: ', poisk)
        print(denet_hranilishe[poisk])

def froze(x,y):
    global blockchain
    global froze
    global end
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO','Заморозка + стэйкинг')
        amount = int(input('сумма заморозки: '))
        if amount <= balance[login]:
            balance[login] = balance[login] - amount
            print('ЗАМОРОЗКА УСПЕШНО ЗАВЕРШЕНА!!! заморозка с кошелька: ',login,'в сумме:',amount,'ROOTOO')
            blockchain = (blockchain,froze,login,amount,end)
            profit = amount/10
            sleep(100)
            balance[login] = balance[login] + amount + profit
        else:
            print('Извините но на вашем балансе не достатачно средств.')
    else:
        print('Вы не вошли в аккаунт')

def change_password(x,y):
    
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт, меняйте пароль', login,'/',balance[login],'ROOTOO')
        new_password = int(input('введите новый пароль -): '))
        print('Ваш новый пароль:', new_password)
        sleep(1)
        print('ОБРАБОТКА...')
        sleep(1)
        accounts[login] = new_password
        print('Пароль успешно изменён!!!')
    else:
        print('Вы ввели неправильный логин/пароль')
        


t1.onclick(login)
t2.onclick(logup)
t3.onclick(send)
t4.onclick(rootooscan)
t5.onclick(denet)
t6.onclick(froze)
t7.onclick(change_password)
mainloop()

_______________________________________________________________________________________________________________________________________________________________________

Version 1.9

from turtle import*
from random import*
from time import*
speed(0)
ids = 0
sites = 0
froze = ('<function froze>')
t1 = Turtle()
t2 = Turtle()
t3 = Turtle()
t4 = Turtle()
t5 = Turtle()
t6 = Turtle()
t7 = Turtle()
t1.shape('square')
t2.shape('square')
t3.shape('square')
t4.shape('square')
t5.shape('square')
t6.shape('square')
t7.shape('square')
t1.penup()
t2.penup()
t3.penup()
t4.penup()
t5.penup()
t6.penup()
t7.penup()
t2.left(90)
t2.forward(50)
t2.right(90)
t3.left(90)
t3.forward(100)
t3.right(90)
t4.left(90)
t4.forward(150)
t4.right(90)
t5.left(90)
t5.forward(200)
t5.right(90)

t6.right(90)
t6.forward(50)
t6.left(90)
t7.right(90)
t7.forward(100)
t7.left(90)

t1.write('    посмотреть баланс', font=('Arial', 14, 'normal'))
t2.write('    создать', font=('Arial', 14, 'normal'))
t3.write('    отправить', font=('Arial', 14, 'normal'))
t4.write('    Rootoo Scan', font=('Arial', 14, 'normal'))
t5.write('    Denet Browser', font=('Arial', 14, 'normal'))
t6.write('    Froze and Stake', font=('Arial', 14, 'normal'))
t7.write('    Поменять Пароль', font=('Arial', 14, 'normal'))
accounts = {}
balance = {}
denet_hranilishe = {}
login = 'id'
sending = (':send ')
end = (' >>')
blockchain = [balance]
nomer = 0
otpravitel = {}
poluchatel = {}
summa = {}
kosel = ('Ваш баланс: ')

staker = {}
staking_balance = {}
stake_block = 0

def logup(x,y):
    global ids
    accounts[ids] = randint(100000, 999999)
    print(ids,accounts[ids])
    balance[ids] = 1
    ids = ids + 1
def login(x,y):
    global kosel
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',kosel,balance[login],'ROOTOO')
    else:
        print('Вы не вошли в аккаунт')
def send(x,y):
    global blockchain
    global sending
    global end
    global otpravitel
    global poluchatel
    global summa
    global nomer
    login = int(input('Введите ID(для отправления Rootoo): '))
    password = int(input('Введите пароль(для отправления Rootoo): '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO','отправление ROOTOO')
        amount = int(input('сумма отправления: '))
        if amount <= balance[login]:
            deposit = int(input('адрес получателя: '))
            balance[login] = balance[login] - amount
            balance[deposit] = balance[deposit] + amount
            print('перевод успешно завершён!!! отправления с кошелька: ',login,'на кошелёк: ',deposit,'в сумме:',amount,'ROOTOO')
            otpravitel[nomer] = login
            poluchatel[nomer] = deposit
            summa[nomer] = amount
            blockchain = (blockchain,nomer,sending,login,deposit,amount,end)
            print('номер транзакции:', nomer)
            otpravitel[nomer] = login
            poluchatel[nomer] = deposit
            summa[nomer] = amount
            nomer = nomer + 1
        else:
            print('Извините но на вашем балансе не достатачно средств.')
    else:
        print('Вы не вошли в аккаунт(для отправления Rootoo)')

def rootooscan(x,y):
    global blockchain
    vibor = input('напишите цифру действия для выполнения \n 1 - просмотр транзакции по номеру \n 2 - просмотр стэйкинга по номеру \n 3 - посмотреть баланс пользователя по адресу \n 4 - посмотреть весь блокчейн: ')
    if vibor == '1':
        tranza = int(input('введите номер транзакции: '))
        print('с адреса: ')
        print(otpravitel[tranza])
        print('на адрес: ')
        print(poluchatel[tranza])
        print('сумма отправления: ')
        print(summa[tranza])
    elif vibor == '2':
        staking = int(input('введите номер Staking_block: '))
        print('Адресс стэйкера: ')
        print(staker[staking])
        print('сумма стэйкинга: ')
        print(staking_balance[staking])
    elif vibor == '3':
        adress = int(input('Введите адрес пользователя: '))
        print(blockchain[adress])
    elif vibor == '4':
        print(blockchain)
def denet(x,y):
    global sites
    vibor = input('Что сделать? создать новый denet ?- тогда напиши -denet- / если просто поиск - то нажми -ENTER- ')
    if vibor == "denet":
        k1 = input('пишите код denet сайта: ')
        denet_hranilishe[sites] = k1
        print('Адрес вашего сайта: ', sites)
        sites = sites + 1
    else:
        poisk = int(input('Введите ссылку на denet: '))
        print('Вы зашли на denet: ', poisk)
        print(denet_hranilishe[poisk])

def froze(x,y):
    global blockchain
    global froze
    global end
    global stake_block
    login = int(input('Введите ID(для заморозки Rootoo): '))
    password = int(input('Введите пароль(для заморозки Rootoo): '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт', login,'/',balance[login],'ROOTOO','Заморозка + стэйкинг')
        amount = int(input('сумма заморозки: '))
        if amount <= balance[login]:
            balance[login] = balance[login] - amount
            print('ЗАМОРОЗКА УСПЕШНО ЗАВЕРШЕНА!!! заморозка с кошелька: ',login,'в сумме:',amount,'ROOTOO')
            blockchain = (blockchain,froze,login,amount,end)
            staker[stake_block] = login
            staking_balance[stake_block] = amount
            print('Staking_block: ',stake_block)
            stake_block = stake_block+1
            profit = amount/10
            sleep(100)
            balance[login] = balance[login] + amount + profit
        else:
            print('Извините но на вашем балансе не достатачно средств.')
    else:
        print('Вы не вошли в аккаунт')

def change_password(x,y):
    
    login = int(input('Введите ID: '))
    password = int(input('Введите пароль: '))
    if accounts[login] == password:
        print('Вы вошли в аккаунт, меняйте пароль', login,'/',balance[login],'ROOTOO')
        new_password = int(input('введите новый пароль -): '))
        print('Ваш новый пароль:', new_password)
        sleep(1)
        print('ОБРАБОТКА...')
        sleep(1)
        accounts[login] = new_password
        print('Пароль успешно изменён!!!')
    else:
        print('Вы ввели неправильный логин/пароль')
        


t1.onclick(login)
t2.onclick(logup)
t3.onclick(send)
t4.onclick(rootooscan)
t5.onclick(denet)
t6.onclick(froze)
t7.onclick(change_password)
mainloop()
    
______________________________________________________________________________________________________________________________________________________________________

Version 2.0
