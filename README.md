# Python-project
class hotel:
    print ("*****WELCOME TO MOHAN'S HOTEL*****")
    print()


    def __init__(self,gt=0,tt=0,v=0,n=0): #Initialising parameters which can use in veg,non veg and display methods
        self.gt=gt
        self.tt=tt
        self.n=n
        self.v=v


    def veg(self): # Show veg menu and ask choice and Quantity

        print("*****VEG MENU*****")

        print("1.wada sambar----->Rs40","2.Vadapao----->Rs15","3.Samosa--->Rs15","4.Thali---->Rs150","5.Chai--->Rs10","6.Exit")
        c=int(input("Enter your choice: "))
        if (c==1):
            d=int(input("Enter the quantity: "))
            self.v=self.v+40*d

        elif (c==2):
            d=int(input("Enter the quantity: "))
            self.v=self.v+15*d

        elif (c==3):
            d=int(input("Enter the quantity: "))
            self.v=self.v+15*d

        elif (c==4):
            d=int(input("Enter the quantity: "))
            self.v=self.v+150*d

        elif (c==5):
            d=int(input("Enter the quantity: "))
            self.v=self.v+10*d

        else:
            print("Not Available")
       
    def nonveg(self): # Show non veg menu and ask choice and Quantity
        print("*****NON-VEG MENU*****")
        print("1.Butter Chicken----->Rs240","2.Mutton Kabab----->Rs100","3.AndaMasal--->Rs80","4.NONVEG Thali---->Rs200","6.Exit")
        c=int(input("Enter your choice: "))

        if (c==1):
            d=int(input("Enter the quantity: "))
            self.n=self.n+40*d

        elif (c==2):
            d=int(input("Enter the quantity: "))
            self.n=self.n+15*d

        elif (c==3):
            d=int(input("Enter the quantity: "))
            self.n=self.n+15*d

        elif (c==4):
            d=int(input("Enter the quantity: "))
            self.n=self.n+150*d
     
        else:
            print("Not Available")

       
    def display(self): #calcute total bill 
        self.gt=self.v+self.n
        print("Your Cost for ordered food is",self.gt,"Rs")
        self.tt=self.gt+(self.gt)*(8/100)
        print("Your total Bill is :",self.gt,"Rs","+","Service Tax:- 8%","=",int(self.tt),"Rs")
              

h=hotel()
def menu():
    opt='y'
    while(opt is 'y' ):
        ch=int(input("Enter your Choice: 1.veg------ 2.Nonveg------- :- "))
        if(ch==1):
            h.veg()
        elif(ch==2):
            h.nonveg()
        else:
            print("invalid option")
        opt=input(("Sir/Madam Do you want order again(y/n)? ")) #enter the loop again if opt is equal to 'y' otherwise exit the loop
    h.display()
print("Thanks For coming to MOHAN'S HOTEL")
menu()
