import mysql.connector

def Add():

mydb mysql.connector.connect(host="localhost", user= "root", password="mysql", database="project")

mycur mydb.cursor()

ch="y":

while ch=="y" or ch=="Y":

eno int(input("Enter Employee No: "))

ename input("Enter Employee Name: ")

dept input("Enter The Department name: ")

desig input("Enter The Designation: ")

salary int(input("Enter The salary: "))

mobile int(input("Enter The mobile no: "))

address input("Enter The address: ")

email input("Enter The email id: ")

str = "INSERT INTO EMP1 values({},"{}","{}","{}",(0,0,"0", "()")"

query (str.format(eno,ename, dept, desig, salary, mobile,

address, email))

mycur.execute(query)

mydb.commit()

print("\n Record inserted \n")

ch= input("Want to Add more record(y/n):")

def search():

mydb mysql.connector.connect(host="localhost", user="root", password="mysql", database="project")

mycur mydb.cursor()

eno int(input("Enter Employee No: "))

str = "SELECT from empl where eno={}"

query (str.format(eno)

print("=

)

mycur.execute(query)

myrec mycur.fetchall()

for x in myrec:

eno x[0]

ename = x[1]

dept * x[2]

desig = x[3]

sal x[4]

mobile =* [5]

address = x[6]

email = x[7]

print ( eno ,^ = ename,, dept,", desig,"", salary,"

",mobile,, address," "email)
