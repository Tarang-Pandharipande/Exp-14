# Experiment 14

**Aim:**  
To explore and apply the concept of inheritance.  
<br>
**Theory:**  
A child class can acquire attributes and behaviors from another class, referred to as the parent class. This core object-oriented concept is known as _inheritance_.  
There are three modes of inheritance:  
&#8594; Public Inheritance  
&#8594; Private Inheritance  
&#8594; Protected Inheritance  
<br>
_Public Inheritance:_  
In public inheritance, the public and protected members of the base class retain their visibility as public and protected in the derived class.  
<br>
_Protected Inheritance:_  
With protected inheritance, the public and protected members of the base class are accessible as protected in the derived class.  
<br>
_Private Inheritance:_  
In private inheritance, both public and protected members of the base class become private members in the derived class.  
<br>
<br>
There are primarily 4 types of inheritance:  
_Single Inheritance:_  
A derived class inherits from only one parent class.  
_Multiple Inheritance:_  
A derived class inherits from multiple parent classes.  
_Multilevel Inheritance:_  
A class inherits from a derived class, forming a multilevel chain of inheritance.  
_Hierarchical Inheritance:_  
Multiple child classes inherit from a single parent class.  

**Code:**
14.a
```
#include <iostream>
#include <string>
using namespace std;

class Uni {
    public:
    string uni = "Symbiosis: ";
    void discipline(){
        cout<<"Engineering"<<endl;
    }
};
class Dep: public Uni {
    public:
    string dept="Electronics & TeleCommunication";
};

int main(){
    Dep u1;
    u1.discipline();
    cout<<u1.uni+" "+u1.dept;
}
```
14.b
```
#include <iostream>
#include <string>
using namespace std;

// Parent Class-1
class Vehicle {
    public:string company = "Ford";
    void type() {
        cout << "Mustang" << endl;
    }
};

// Parent Class-2
class Specs {
public:
    string mileage = "8 km/l";
    
    void colour() {
        cout << "Grey" << endl;
    }
};

// Child Class (derived from both Vehicle and Specs)
class Car : public Vehicle, public Specs {
public:
    string seater = "4 seater";
};

int main() {
    Car f2;
    
    f2.colour(); 
    cout << f2.company << endl; 
    f2.type(); 
    cout << "(" << f2.seater << ")" << endl; 
    cout << "MILEAGE: " << f2.mileage << endl; 

    return 0;
}
```

14.c

```
#include <iostream>
#include <string>
using namespace std;

// Parent Class-1
class Food {
public:
    string cuisine = "Indian";
    
    void type() {
        cout << "Asian" << endl;
    }
};

// Child Class-1 (derived from Parent-1)
class Dish : public Food {
public:
    string dish = "Biryani";
};

// Child Class-2 (derived from Child-1)
class Restaurant : public Dish {
public:
    string name = "Spice Kitchen";
};

int main() {
    Restaurant f3;
    
    f3.type();  
    cout << f3.cuisine << ": " << f3.dish << endl;   
    cout << "Restaurant: " << f3.name << endl;  

    return 0;
}
```

14.d

```
#include <iostream>
#include <string>
using namespace std;

//Parent Class-1
class Jeans {
    public:
    string type[3]= {"Bootcut", "Wide Leg", "Skinny"};
    void brand(){
        cout<<"H&M - &Denim"<<endl;
    }
};
//Child Class-1
class Bootcut: public Jeans {
    public:
    string color="Dark Blue";
};
//Child Class-2
class WL: public Jeans {
    public:
    string color="Black";
};
//Child Class-3
class Skinny: public Jeans {
    public:
    string color="Grey";
};

int main(){
    Bootcut j1;
    cout<<endl;
    j1.brand();
    cout<<j1.type[0]<<": "<<j1.color<<endl;

    WL j2;
    cout<<endl;
    j2.brand();
    cout<<j2.type[1]<<": "<<j2.color<<endl;

    Skinny j3;
    cout<<endl;
    j3.brand();
    cout<<j3.type[2]<<": "<<j3.color<<endl;
}
```
**Output:**
14.a ![image_2024-10-21_091919232](https://github.com/user-attachments/assets/59f7acc2-6fd3-446c-bb13-b311950156bf)

14.b ![image_2024-10-21_092001086](https://github.com/user-attachments/assets/ab80071c-d590-48a7-94b1-2638a4dd3f85)

14.c ![image_2024-10-21_092022773](https://github.com/user-attachments/assets/3d14356b-c5b2-47b4-96e2-138bc7fdc302)

14.d ![image_2024-10-21_092036110](https://github.com/user-attachments/assets/b4bc3835-ae1f-4077-96f6-fbd2bde6c44a)

<br>

**Conclusion:** <br>
&#8594; We learnt about inheritance in C++. <br>
&#8594; We learnt the types and modes of inheritance in C++. <br>
*******
<br>
