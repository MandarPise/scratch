# <a name="main"></a>Object oriented programming core concepts

8 Aug 2021

Editor:
* [Mandar Pise]

Comments and suggestions for improvement are most welcome.

Object Oriented Programming System:

* [Ab: Abstraction](#S-abstraction)
* [En: Encapsulation](#S-encapsulation)
* [In: Inheritance](#S-inheritance)
* [Po: Polymorphism](#S-polymorphism)

# <a name="S-abstraction"></a>Ab: Abstraction

Abstraction means displaying only essential information and hiding the details
Providing only essential information to outside world and hiding the background
details or implementation.

# <a name="S-encapsulation"></a>En: Encapsulation

The process of binding data members (variables, properties) and functions
(methods) into a single unit. Data members and functions are encapsulated in a
class.

# <a name="S-inheritance"></a>In: Inheritance

An object or class can be based on another object or class. Inheritance allows
Creating new classes that reuse, extend and modify the behavior that is defined
in other classes. A class that is inherited is called the base class and the
class that inherits is called the derived class.

# <a name="S-polymorphism"></a>Po: Polymorphism

Poly means Many and Morphism means Forms.
A concept that provides the ability of objects to take on multiple types.

There are two types of Polymorphism:
* [En.Static: Static or Compile-time](#SS-static)
* [En.Dynamic: Dynamic or Runtime](#SS-dynamic)

## <a name="SS-static"></a>En.Static: Static or Compile-time

Static or compile time Polymorphism

Functionality is decided at the compile time. Function overloading.

eg. Function overloading

    class Sample
    {
      public:
        void add(int a, int b)
        {
          // do something
        }

        void add(string s1, string s2)
        {
          // do something
        }
    };

Here add function is overloaded which add function to call is decided at compile
time hence it is compile time polymorphism.

## <a name="SS-dynamic"></a>En.Dynamic: Dynamic or Runtime

Dynamic or Run time Polymorphism

Functionality is decided at the run time. Function overriding.

eg. Function overriding

    class Base
    {
      public:
        virual void display()
        {
          // do something
        }
    };

    class Derived : public Base
    {
      public:
        void display() override // ovedrride keyword is added in c++ 11.
        {
          // do something
        }
    };

    int main()
    {
      Base *pBase = new Base;
      pBase.display(); // Function from Base class is called as object is of base type.

      pBase = new Derived;
      pBase.display(); // Function from Derived class is called as object is of Derived type.

      return 0;
    }

Which display() function to call is decided at runtime so this is called as runtime
polymorphism.