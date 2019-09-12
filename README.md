import os 
booklist = list()

menu = """
[1] Add a Book
[2] Have a Book
[3] List All Books
[Q] Quit
"""
def addbook(book:tuple,list:list) :
    list.append(book)
    print("Please press Enter to back to the menu")
    input()
    
def havebook(book:tuple,list:list) :
    if book in list :
        list.remove(book)
        print("Please press Enter to back to the menu")
        input()
    if book not in list :
        print("There is no book like that one")
        print("Please press Enter to back to the menu")
        input()
        
def listbook(list:list) :
    for i in list :
        print("Book Name, Writer Name, Book Place) :".format(i)
    print("Please press Enter to back to the menu")
    input()    
      
      
def cik() :
    print("Quited..!")
    print("Please press Enter to back to the menu")
    input()
    
while True :
    os.system("cls")
    print(menu)
    
    x = input("Select Anything You Want :")
    
    if x == "1" :
        bookname =   input("Book Name   :")
        writername = input("Writer Name :")
        placebook =  input("Book Place  :")
        book = (bookname, writername, placebook)
        addbook(book,booklist)
        
    elif x == "2" :
        bookname =   input("Book Name   :")
        writername = input("Writer Name :")
        placebook =  input("Book Place  :")
        book = (bookname, writername, placebook)
        havebook(book,booklist)
        
    elif x == "3" :
        listbook(booklist)
        
    elif x == "q" or x == "Q" :
        cik()
        
    else :
        print("Please enter valid value..!")
        print("Please press Enter to back to the menu")
        input()
        
    
        
        
