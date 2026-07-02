layout: page
title: "Decorators in Python"
permalink: /python/decorator

Let’s say you run a bakery. You prepare cakes on order.
You are asked for a Vanilla cake. You bake it and decorate it with whipping cream.
You are asked for a butterscotch cake. You bake it and decorate it with whipping cream.
You are asked for a chocolate cake. You bake it and decorate it with whipping cream.

Now, you bake each cake separately as the procedure is different for each of them. But the decor? Since it is the same whipping cream, you don’t prepare it every time you get a cake order. You keep the prepared whipping cream and get it to decorate every time you bake a cake. 
This is exactly what a decorator in python can do!

You have a function, you want to enhance its behaviour but not change the function itself - you use a decorator. 

A decorator is also a function which accepts another function and returns by wrapping it with some enhancement.

Here is a sample code for the above process.

Each function below specifically has process to bake that particular cake.

def vanilla_cake():
    print("Baking vanilla cake")


def chocolate_cake():
    print("Baking chocolate cake")    
    
def butterscotch_cake():
    print("Baking butterscotch cake”)

Now, we want to decorate it with whipping cream.


def whipping_cream():        
	print("spread whipping cream on the given cake")

One way of doing this without decorators, is by just calling the whipping_cream function inside each cake.

def vanilla_cake():
    print("Baking vanilla cake”)
    whipping_cream()


def chocolate_cake():
    print("Baking chocolate cake")   
    whipping_cream() 
    
def butterscotch_cake():
    print("Baking butterscotch cake”)
    whipping_cream()

But, here are changing the actual function to enhance it. To d it with out touching the function from inside, we use decorators.

In a decorator, we accept the actual function and wrap it with our enhancement and return it.

def whipping_cream(func):
    def wrap():
        func()
        print("spread whipping cream on the given cake")
     
    return wrap

To decorate a function. With it, we simply use @ annotation while defining the function.

@whipping_cream
def vanilla_cake():
    print("Baking vanilla cake")

@whipping_cream
def chocolate_cake():
    print("Baking chocolate cake")    
    
@whipping_cream
def butterscotch_cake():
    print("Baking butterscotch cake”)

vanilla_cake()
chocolate_cake()
butterscotch_cake()

Output:
Baking vanilla cake
spread whipping cream on the given cake
Baking chocolate cake
spread whipping cream on the given cake
Baking butterscotch cake
spread whipping cream on the given cake


We can pass arguments to a decorator.

Here is code where the functions accept the weight of cake in grams as argument for the function.

def whipping_cream(func):
    def wrap(g):
        func(g)
        print("spread whipping cream on ",g," grams", " cake")
        
    return wrap


@whipping_cream
def vanilla_cake(g):
    print("Weight=",g," grams")
    print("Baking vanilla cake")

@whipping_cream
def chocolate_cake(g):
    print("Baking chocolate cake")    
    
@whipping_cream
def butterscotch_cake(g):
    print("Baking butterscotch cake")



vanilla_cake(500)
chocolate_cake(1000)
butterscotch_cake(1000)   

Output:

Weight= 500  grams
Baking vanilla cake
spread whipping cream on  500  grams  cake
Baking chocolate cake
spread whipping cream on  1000  grams  cake
Baking butterscotch cake
spread whipping cream on  1000  grams  cake



