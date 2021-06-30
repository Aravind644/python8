# python8
ACCESS MODIFIERS


1. Create a class with PRIVATE fields, private method and a main method. Print the fields
in main method. Call the private method in main method.
Create a sub class and try to access the private fields and methods from sub class.


class First:
    def __init__(self,x,y):
        self.a=x
        self.__b=y
        return
    def main():
        obj=First(5,10)
        print('a val:',obj.a)
        print('b val:',obj.__b)
        return
First.main()


*  In we cannot access private method from subclass.




2.Create a class with DEFAULT fields and methods. Access these fields and methods
from any other class in the same package


class First:
    __a=10
    def getA():
        return First.__a
class second:
    def main():
        print('a val:',First.getA())
        return
second.main()




3. Create a class with PROTECTED fields and methods. Access these fields and methods
from any other class in the same package.
Also, Access the PROTECTED fields and methods from child class located in a different
package
Access the PROTECTED fields and methods from any class in different package


class Parent(object):
    def _protected(self):
        print('It is protected')

class Child(Parent):
    def foo(self):
        self._protected()

c = Child()
c._protected()



4. Create a class with PUBLIC fields and methods.
Access the public methods and fields from any class in the same package or different
package.


class Test:
    a=10
    def __init__(self,b):
        self.b=b
        return
class Access:
    def main():
        obj=Test(20)
        print('a val:',Test.a)
        print('b val:',obj.b)
        return
Access.main()
    
