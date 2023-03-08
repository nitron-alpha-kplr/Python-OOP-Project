- Nous allons a présent créer une classe InventoryProductEntry qui a pour role de représenter une entrée d'inventaire pour un produit spécifique.
- Après avoir créer les différentes classes qui modélisent les produits de notre magasin, nous devons créer du code qui permet de gérer nos produits et leur inventaire.
- Cette classe nous permettra de stocker des informations telles que la quantité en stock, les revenues et les dépenses liées à ce produit.
- Donc, elle permet de gérer le stock lié à un seul produit.


#debut de l'exercice


class InventoryProductEntry:

def __init__(self, nom, code):
self.__nom = nom du produit
self.__code = code
def Stocker(self, code):
if self.__Code < quantité :
raise ValueError("quantité insuffisante")
self.__nom produit -=stock
def afficher_sstock(self):
print("L'inventaire du stock de", self.__nom, "est de", self.__solde, "quantité")





#ce code je l'ai trouve sur stackoverflow , je l'ai mis a titre informatif pour moi !!!!#

 self.name = name
        self.price = price
        self.date = date
        self.supplier = supplier
        self. quantity = quantity

    def check_item(self, name):
        for i in range(len(ls)):
            if (ls[i].name == name):
                return i

    def sale(self):
        n = int(input("How many products to sale: "))
        total = 0
        for j in range(n):
            name = input("Enter Product name : ")
            quantity = int(input("Enter quantity: "))
            i = obj.check_item(name)
            if i and ls[i].quantity >= quantity:
                ls[i].quantity -= quantity
                if ls[i].quantity < 5:
                    print("Low Stock! Low Stock! Order Placed")
                    obj.place_order(name, ls[i].supplier, quantity+10)
                print("....Uncle G Shop....")
                print(datetime.date.today())
                print("Product Name  | Quantity  | Cost $")
                print(ls[i].name, end=" ")
                print(quantity, end=" ")
                print(ls[i].price * quantity)
                total += ls[i].price * quantity
                print("\n")
                print("Total Cost----->", "$" + total)
            else:
                print("Product out of stock or not enough quantity")


    def purchase(self):
        name = input("Enter Product name: ")
        date = datetime.date.today()
        i = obj.check_item(name)
        if i:
            ls[i].quantity += int(input("Enter quantity: "))
            ls[i].price = int(input("Enter product price: "))
            ls[i].date = date
        else:
            quantity = int(input("Enter quantity: "))
            price = int(input("Enter product price: "))
            supplier = input("Enter Supplier: ")
            ob = Stock(name, price, supplier, quantity, date)
            ls.append(ob)


    def place_order(self,name, supplier, quantity):
        return name, supplier, quantity

    def print_products(self):
        def __repr__(self):
            return str(self.name) + str(self.price) + str(supplier) + str(self.quantity) + str(self.date)
        return __repr__

    def main(self):
        print("Welcome To Uncle G Shop")
        print("choose an option below")
        print("\n1.Enter a Product\n2.Make a sale \n3.See all Products\n4.Exit")
        option = int(input("Enter option here: "))
        while True:
                

            if option == 1:
                obj.purchase()
            elif option == 2:
                obj.sale()
            elif option == 3:
                obj.print_products()
            elif option == 4:
                print("Have a good day")
                break
            else:
                print("Enter a valid input!")
# A list to add Products
ls = []

# an object of Stock class
obj = Stock('', 0, 0, 0, '')
obj.main()












def write_content(content,filename):
        with open(filename, "w", encoding='utf-8') as f:
            f.write(content)